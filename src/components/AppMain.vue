<script>
import SingleComic from './SingleComic.vue';
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
            ],
            dataComic :[
                {
                    thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    series: "Action Comics",
                    "type": "comic book",
                },
                {
                    thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    series: "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    series: "Aquaman",
                    "type": "graphic novel",
                },
                {
                    thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    series: "Batgirl",
                    "type": "comic book",
                },
                {
                    thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    series: "Batman",
                    "type": "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    series: "Batman Beyond",
                    "type": "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    series: "Batman/Superman",
                    "type": "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    series: "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    series: "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    series: "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    series: "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    series: "Catwoman",
                    "type": "graphic novel",
                },
]
        };
    },
    components: {
        SingleComic
    }
}
</script>

<template>
    <main>
        <div  class="bg-comic">
            <div>
                <button class="button">
                    Current series
                </button>
            </div>
        </div>
        <div class="bg-top">
            <div class="container">
                <div class="jumbotron">
                    <SingleComic
                    v-for="(singleComicPost, i) in dataComic" :key="i" 
                    :title="singleComicPost.series"
                    :image="singleComicPost.thumb"/>
                </div>  
                <div class="text-align">
                    <button class="button-special">
                        Load More
                    </button>
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
    .bg-comic{
        height: 250px;
        background-image: url(../../public/img/jumbotron.jpg);
        background-size: 100% auto; 
        position: relative;
        .button {
                background-color: #0282F9;
                border: none;
                color: white;
                padding: 15px;
                text-align: center;
                text-decoration: none;
                font-size: 16px;    
                text-transform: uppercase;
                font-weight: bold;
                position: absolute;
                bottom: -10%;
                left: 5%;
            }  
    }
    .bg-top{
        background-color: #1C1C1C
    }
    .bg-bot{
        background-color: $bg-blue
    }
    
    
    .container{
        @include my-container ;
        .jumbotron{
            display: flex;
            flex-wrap: wrap;
            padding-top: 40px;   
        }
        .text-align{
            text-align: center;
            padding-bottom: 20px;
        }
        .button-special {
                background-color: #0282F9;
                border: none;
                color: white;
                padding: 15px;
                text-align: center;
                text-decoration: none;
                font-size: 16px;    
                text-transform: uppercase;
                font-weight: bold;
                
               
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
