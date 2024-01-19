<script>

export default {
    data() {
        return {
            navBar:[
                {
                navLink: 'Character',
                link:'#'
            },
            {
                navLink: 'Comics',
                link:'#'
            },
            {
                navLink: 'Movie',
                link:'#'
            },
            {
                navLink: 'Tv',
                link:'#'
            },
            {
                navLink: 'Games',
                link:'#'
            },
            {
                navLink: 'Collectibles',
                link:'#'
            },
            {
                navLink: 'Videos',
                link:'#'
            },
            {
                navLink: 'Fans',
                link:'#'
            },
            {
                navLink: 'News',
                link:'#'
            },
            {
                navLink: 'Shop',
                link:'#'
            }
        ],
        };
    },
    methods: {

    }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="padding">
                <img src="/img/dc-logo.png" alt="">
            </div>
            <nav> 
                <ul class="list-unstyled">
                    <li v-for="(item,i) in navBar">
                        <a :href="item.link">
                            {{ item.navLink }}
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use  "../assets/scss/partials/mixins.scss" as *;

header{
    .container{
    display: flex;
    justify-content: space-between;
    align-items: center;
   
    @include my-container
    
    
}
ul{
    display: flex;
}
.padding{
    padding: 10px;
}
li{
    padding: 10px;
    
    &:hover{
        
        border-bottom: 10px solid blue;
    }
    a{
        text-decoration: none;
        color: black;
        text-transform: uppercase;
        font-weight: bold;
        
    }
}
.list-unstyled{
    list-style: none;
}
}
</style>
