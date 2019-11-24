<template>
<div >

    
    <b-container >
            <h1>Products Page One</h1>
        <b-row  >
            <ProductItem v-for='(product, index) in products' v-bind:key="index"
                :name='product.name'
                :price='product.price'
                :img='product.img'
                :productIndex='index'
                ></ProductItem>

        </b-row>
        

     

    </b-container>
</div> 
</template>

<script>
import ProductItem from '../components/ProductItem.vue';

export default {
    data(){
        return { 
            products:[
                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=8'
                },
                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=4'
                },

                 {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=42'
                },
                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },

                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=68'
                },
                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=28'
                },

                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },
                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=78'
                },

                 {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=38'
                },
                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=78'
                },

                 {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },
                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },

                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },
                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },

                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },
                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },

                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },
                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },

                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },
                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },

                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },
                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },

                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },
                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },

                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },
                {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },

                 {
                name:'Shoe one',
                price:'2,000',
                img:'https://picsum.photos/600/300/?image=48'
                },
                

            ]
            }
    },
    computed:{
        
    },
 
 components:{
    ProductItem
 }
    
}
</script>

<style >

</style>