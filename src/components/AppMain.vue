<script>
export default {
    data() {
        return {

        };
    },
    methods: {

    }
}
</script>

<template>
    <main>
        <div class="container">
            <div class="jumbotron">
                content qui
            </div>

            <div class="bg-blue">
                aaaa 
            </div>
            
        </div>
        
    </main>
</template>

<style lang="scss" scoped>
@use  "../assets/scss/partials/mixins.scss" as *;
main{
    // @include my-container
    .container{
        @include my-container
    }
        .jumbotron{
        width: 100%;
        height: 120px;
        background-color: #1C1C1C;
        padding: 20px;
        text-align: center;
        color: white;
        }
        .bg-glue{
        width: 100%;
        height: 300px;
        padding: 20px;
        background-color: #0282F9;
        }
}

</style>
