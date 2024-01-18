<script>
export default {
    data() {
        return {
            dataImg: [
                {
                    img:'img/buy-comics-digital-comics.png',
                    description: 'DIGITAL COMICS'
                },
                {
                    img:'img/buy-comics-merchandise.png',
                    description: 'DC MERCHANDISE'
                },
                {
                    img:'img/buy-comics-subscriptions.png',
                    description: 'SUBSCRPTION'
                },
                {
                    img:'img/buy-comics-shop-locator.png',
                    description: 'COMIC SHOP LOCATOR'
                },
                {
                    img:'img/buy-dc-power-visa.svg',
                    description: 'DC POWER VISA'
                },
            ]
        };
    },
    methods: {

    }
}
</script>

<template>
    <main>
        
        <div class="bg-top">
            <div class="container">
            <div class="jumbotron">
                content qui
            </div>              
        </div>
        </div>
        <div class="bg-bot">
            <div class="container">
            <div class="bg-blue">
                <ul class="list-unstyled">
                    <li v-for ="(singleImg ,i) in dataImg">
                        <div class="img-box">
                            <img :src="singleImg.img" alt="">
                        </div>
                        <div class="flex">
                            {{ singleImg.description }}
                        </div>
                    </li>
                </ul>
            </div>
        </div>
        </div>
        
    </main>
</template>

<style lang="scss" scoped>
@use  "../assets/scss/partials/mixins.scss" as *;
@use  "../assets/scss/main.scss" as *;

main{
    .bg-top{
        background-color: #1C1C1C
    }
    .bg-bot{
        background-color: $bg-blue
    }
    
    // @include my-container
    .container{
        @include my-container ;
        .jumbotron{
        width: 100%;
        height: 120px;
        // background-color: #1C1C1C;
        padding: 20px;
        text-align: center;
        color: white;
        }

        .bg-blue{
        width: 100%;
        height: 100px;
        padding: 20px;
        // background-color: #0282F9;
        }
        .list-unstyled{
            list-style: none;
        }
        .img-box{
            width: 50px;
            height: 50px;
        }
        img{
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
        ul{
            display: flex;
            align-items: center;
            justify-content: center;
            
        }
        li{
            display: flex;
            margin-left: 20px;
            
        }
        .flex{
            display: flex;
            align-items: center;
            margin-left: 20px;
        }
    }
        
        
}


</style>
