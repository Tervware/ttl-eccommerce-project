<template>
   <div>
<!-- Banner -->
<div class="img">
   <h1 class="text-center text-white"> Welcome to TTL Online Store</h1>
</div>

<!-- Products -->
<b-container class="mt-5">
    <h1>Our Products</h1>
<b-row>
   <ProductItem v-for="(product,index) in products" :key="index"
     :name="product.name" 
     :price="product.price"
     :img="product.image"
     :productIndex="index"
    />
    

</b-row>
</b-container>



   </div>
</template>

<script>
import ProductItem from '../components/ProductItem.vue';

export default {
    data(){
        return{ 
            products:[
                {
                name:'Product Zero',
                price:200000,
                image:"https://picsum.photos/600/300/?image=26"
                },
                 {
                name:'Product Zero',
                price:200000,
                image:"https://picsum.photos/600/300/?image=25"
                },
                 {
                name:'Product Zero',
                price:200000,
                image:"https://picsum.photos/600/300/?image=28"
                },
                {
                name:'Product One',
                price:200000,
                image:"https://picsum.photos/600/300/?image=27"
                },
                {
                name:'Product Two',
                price:500000,
                image:"https://picsum.photos/600/300/?image=26"
                },
                {
                name:'Product One',
                price:200000,
                image:"https://picsum.photos/600/300/?image=35"
                },
                
            ]
        }
    },
    components:{
        ProductItem
    }
}
</script>

<style   scoped>
.img{ 
    padding-bottom: 30vh;
    padding-top: 30vh;
    background-image: url(https://picsum.photos/1024/400/?image=41);
    background-repeat: no-repeat;
    background-size:cover;
}
 
</style>