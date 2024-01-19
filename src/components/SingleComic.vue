<script>
export default {
    data() {
        return {
                      
        };
    },
    props: {
        title: String,
        image: String
    }
}
</script>

<template>
    <div class="single-comic">
        <div class="box-comic-img">
            <img :src="image" :alt="title">
        </div>

        <h5 class="h5-format">
            {{ title }}
        </h5>
    </div>
            
</template>

<style lang="scss" scoped>

        .box-comic-img{
            width: 100px;
            height: 100px;
            img{
                width: 100%;   
                height: 100%;
            }
        }
        .single-comic{
            width: calc((100% / 6 ) - 30px);
            margin-bottom: 70px ;
            margin-right: 30px;
            display: flex;
            flex-direction: column;
            align-items: center;

         }
         .h5-format{
            color: white;
            margin-top: 20px;
            text-transform: uppercase;
            
         }


</style>
