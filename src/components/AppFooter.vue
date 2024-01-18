<script>
export default {
    data() {
        return {
            dataFooterImg:[
                {
                    img:'../../public/img/footer-facebook.png'
                },
                {
                    img:'../../public/img/footer-twitter.png'
                },
                {
                    img:'../../public/img/footer-youtube.png'
                },
                {
                    img:'../../public/img/footer-pinterest.png'
                },
                {
                    img:'../../public/img/footer-periscope.png'
                }
            ]

        };
    },
    methods: {

    }
}
</script>

<template>
    <footer>
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
                <div class="img-dc">
                    <img src="../../public/img/dc-logo-bg.png" alt="">
                </div>
            </div>
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
    </footer>
</template>

<style lang="scss" scoped>
@use  "../assets/scss/partials/mixins.scss" as *;

footer{
    .container{
        @include my-container ;
        .footer-top{
            height: 300px;
            background-image: url(../../public/img/footer-bg.jpg);
            overflow: hidden;
            display: flex;
            // align-items: center;
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
            background-color: #1C1C1C;
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
