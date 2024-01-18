<script>

export default {
    data() {
        return {
            navBar:[
                {
                navLink: 'Character'
            },
            {
                navLink: 'Comics'
            },
            {
                navLink: 'Movie'
            },
            {
                navLink: 'Tv'
            },
            {
                navLink: 'Games'
            },
            {
                navLink: 'Collectibles'
            },
            {
                navLink: 'Videos'
            },
            {
                navLink: 'Fans'
            },
            {
                navLink: 'News'
            },
            {
                navLink: 'Shop'
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
                        {{ item.navLink }}
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss">
@use  "../assets/scss/partials/mixins.scss" as *;

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
    text-transform: uppercase;
    font-weight: bold;
    &:hover{
        color: blue;
        border-bottom: 10px solid blue;
    }
}
.list-unstyled{
    list-style: none;
}
</style>
