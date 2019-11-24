<template>
<div>
<b-container>
   <h1>
        Single Product Page {{productId  }}

    </h1>
    <b-card
                :title="product.name"
                :img-src="product.img" 
                img-top
                tag="article"
                style="max-width: 40rem; margin:auto"
                class="mb-4"
            >
                <b-card-text>
                N {{product.price}} 
                </b-card-text>

                <b-button   variant="primary">Buy Now</b-button>
            </b-card>

</b-container>
 </div>
    
</template>

<script>
export default {
    data(){
        return{
            productId:this.$route.params.productId,

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
        product(){
            return this.products[this.productId];
        }
    }
}
</script>