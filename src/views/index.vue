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
   <ProductItem v-for="product in products" :key="product._id"
     :name="product.name"
     :price="product.price"
     :img="baseUrl+'/'+product.images[0]"
     :productIndex="product._id"
    />


</b-row>
</b-container>



   </div>
</template>

<script>
import axios from 'axios';
import ProductItem from '../components/ProductItem.vue';


export default {
    data(){
        return{
          baseUrl:'http://localhost:3000',
          products:[]
        }
    },
    mounted(){
          axios.get(this.baseUrl+'/products')
          .then( (response)=> {
            // handle success
            this.products = response.data.slice(0,6);
            console.log(response.data);
          })
          .catch(function (error) {
            // handle error
            console.log(error);
          })
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
    background-image: url("../assets/images/banner.jpg");
    background-repeat: no-repeat;
    background-size:cover;
}

</style>
