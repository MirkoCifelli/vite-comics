<script>
export default {
    data() {
        return {
            dataFooterImg:[
                {
                    img:'/img/footer-facebook.png'
                },
                {
                    img:'/img/footer-twitter.png'
                },
                {
                    img:'/img/footer-youtube.png'
                },
                {
                    img:'/img/footer-pinterest.png'
                },
                {
                    img:'/img/footer-periscope.png'
                }
            ],
        //     dataFooterObj:[
        //     {
        //         stringa: 'DC COMICS',
        //     },
        //     {
        //         stringa: 'Character',
        //     },
        //     {
        //         stringa: 'Comics',
        //     },
        //     ,
        //     {
        //         stringa: 'Movier',
        //     },
        //     ,
        //     {
        //         stringa: 'TV',
        //     },
        //     {
        //         stringa: 'Games',
        //     },
        //     ,
        //     {
        //         stringa: 'Videos',
        //     },
        //     {
        //         stringa: 'News',
        //     }
        // ]

        };
    },
    methods: {

    }
}
</script>

<template>
    <footer>
        <div class="bg-special">
            <div class="container">
            <div class="footer-top">
                <div>
                    <ul>
                        <li>
                            DC COMICS
                        </li>
                        <li>
                            Character
                        </li>
                        <li>
                            Comics
                        </li>
                        <li>
                            Movies
                        </li>
                        <li>
                            TV
                        </li>
                        <li>
                            Games
                        </li>
                        <li>
                            Videos
                        </li>
                        <li>
                            News
                        </li>
                    </ul>
                    <ul>
                        <li>
                            SHOP
                        </li>
                        <li>
                            Shop Dc
                        </li>
                        <li>
                            Shop Dc  Collection
                        </li>
                    </ul>
                </div>
                <div>
                    <ul>
                        <li>
                            DC
                        </li>
                        <li>
                            Terms Of Use
                        </li>
                        <li>
                            Privacy policy(New)
                        </li>
                        <li>
                            Ad Choices
                        </li>
                        <li>
                            Advertising
                        </li>
                        <li>
                            Jobs
                        </li>
                        <li>
                            Subscription
                        </li>
                        <li>
                            Talent Workshops
                        </li>
                        <li>
                            CPSC Certificates
                        </li>
                        <li>
                            Ratings
                        </li>
                        <li>
                            Shop Help
                        </li>
                        <li>
                            Contact Us
                        </li>
                    </ul>
                </div>
                <div>
                    <ul>
                        <li>
                            SITES
                        </li>
                        <li>
                            DC
                        </li>
                        <li>
                            MAD Magazine
                        </li>
                        <li>
                            DC Kids
                        </li>
                        <li>
                            DC Universe
                        </li>
                        <li>
                           DC Power Visa
                        </li>
                        
                    </ul>
                </div>
                <!-- <div>
                    <ul>
                        <li v-for="(singlePost , k) in dataFooterObj">
                            <span>
                                {{ singlePost.stringa }}
                            </span>
                        </li>
                    </ul>
                </div> -->
                <div class="img-dc">
                    <img src="../../public/img/dc-logo-bg.png" alt="">
                </div>
            </div>
            
        </div>
        </div>
        <div class="bg-bot">
            <div class="container">
            <div class="footer-botton">
                <div class="button">
                    SING-UP NOW!
                </div>
                <div class="flex">
                    <div class="color">
                        Follow us
                    </div>
                    <div class="flex">
                        <div v-for="(itemFooter, i) in dataFooterImg" >
                            <img :src="itemFooter.img" alt="" class="margin-left">
                        </div>
                    </div>
                </div>
            </div>
        </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use  "../assets/scss/partials/mixins.scss" as *;

footer{
    .bg-special{
        background-image: url(../../public/img/footer-bg.jpg);
    }
    .bg-bot{
        background-color: #1C1C1C
    }
    .container{
        @include my-container ;
        .footer-top{
            height: 300px;
            // background-image: url(../../public/img/footer-bg.jpg);
            overflow: hidden;
            display: flex;
            // align-simglePost: center;
            // justify-content: space-around;
            padding: 20px;
            .img-dc{
                width: 100%;
                margin-left: 350px;
                
            }
            img{
                height: 150%;
            }
            ul{
                list-style: none;
                margin-left: 30px;
            }
            li{
                &:first-child {
                color: white;
                font-weight: bold;
                text-transform: uppercase;
                margin-bottom: 20px;
                margin-top: 20px;
                }
                color: darkgrey;
                font-size: 11px;
            }
        }
        .footer-botton{
            display: flex;
            justify-content: space-between;
            height: 100px;
            // background-color: #1C1C1C;
            padding: 20px;
            .button {
                background-color: #1C1C1C;
                border: 1px solid #0282F9;
                color: white;
                padding: 20px;
                text-align: center;
                text-decoration: none;
                font-size: 16px;    
            }
            .flex{
                display: flex;
                align-items: center;
                
            }
            .color{
                color: #0282F9;
                font-weight: bold;
                text-transform: uppercase;
            }
            .margin-left{
                margin-left: 20px;
            }
        }
    }
}
</style>
