<template>
    <b-col sm="4">

            <div>
            <b-card
                :title="name"
                :img-src="img" 
                img-top
                tag="article"
                style="max-width: 20rem;"
                class="mb-4"
            >
                <b-card-text>
                N {{price}} 
                </b-card-text>

                <b-button @click="gotoSingleProductPage(productIndex)" variant="primary">View Product</b-button>
            </b-card>
            </div>
    </b-col>
</template>

<script>
export default {
    props:[
        'name',
        'price',
        'img',
        'productIndex'
    ],
    methods:{
        gotoSingleProductPage(id){
            this.$router.push('/products/'+id);
        }
    }
}
</script>