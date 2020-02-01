<template>
<div >


    <b-container >
            <h1>Products Page One</h1>
        <b-row  >
            <ProductItem v-for='product in products' v-bind:key="product._id"
                :name='product.name'
                :price='product.price'
                :img='baseUrl+"/"+product.images[0]'
                :productIndex='product._id'
                ></ProductItem>

        </b-row>




    </b-container>
</div>
</template>

<script>
import axios from 'axios';
import ProductItem from '../components/ProductItem.vue';

export default {
    data(){
        return {
            baseUrl:'http://localhost:3000',
            products:[]
            }
    },
    mounted(){
          axios.get(this.baseUrl+'/products')
          .then( (response)=> {
            // handle success
            this.products = response.data;
            console.log(response.data);
          })
          .catch( (error) =>{
            // handle error
            console.log(error);
          })
    },

 components:{
    ProductItem
 }

}
</script>

<style >

</style>
