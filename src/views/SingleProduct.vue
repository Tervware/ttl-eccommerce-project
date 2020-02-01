<template>
    <div>

        <section class="section-components padding-y mt-5">
            <div class="container">

                <output>
                    <div class="card">
                        <div class="row no-gutters">
                            <aside class="col-md-6">
                                <article class="gallery-wrap p-3">
                                    <div class="img-big-wrap">
                                        <div>
                                            <a href="#"><img :src="baseUrl+'/'+product.images[0]"></a>
                                        </div>
                                    </div>
                                    <!-- slider-product.// -->
                                    <div class="thumbs-wrap">
															 
                                         <a class="item-thumb" v-for='image in product.images' :key="image" > <img :src="baseUrl+'/'+image"></a>

                                    </div>
                                    <!-- slider-nav.// -->
                                </article>
                                <!-- gallery-wrap .end// -->
                            </aside>
                            <main class="col-md-6 border-left">
                                <article class="content-body p-3">

                                    <h2 class="title">{{product.name}}</h2>

                                    <div class="mb-3">
                                        <var class="price h4">&#8358; {{product.price}}</var>
                                        <span class="text-muted">/Item</span>
                                    </div>
                                    <!-- price-detail-wrap .// -->

                                    <p> {{product.description}}
                                    <dl class="row">
                                        <dt class="col-sm-3">Processor#</dt>
                                        <dd class="col-sm-9">{{product.specification.processor}}</dd>

                                        <dt class="col-sm-3">Front Camera</dt>
                                        <dd class="col-sm-9">{{product.specification.front}}</dd>

                                        <dt class="col-sm-3">Rear Camera</dt>
                                        <dd class="col-sm-9">{{product.specification.rearCamera}} </dd>
                                    </dl>

                                    <hr>
                                    <div class="form-row">
                                        <div class="form-group col-md flex-grow-0">
                                            <label>Quantity</label>
                                            <div class="input-group mb-3 input-spinner">
                                                <div class="input-group-prepend">
                                                    <button class="btn btn-light" type="button" id="button-plus"> + </button>
                                                </div>
                                                <input type="text" class="form-control" value="1">
                                                <div class="input-group-append">
                                                    <button class="btn btn-light" type="button" id="button-minus"> − </button>
                                                </div>
                                            </div>
                                        </div>
                                        <!-- col.// -->

                                    </div>
                                    <!-- row.// -->

                                    <a href="http://bootstrap-ecommerce.com/developer.html#" class="btn  btn-primary"> Place Order </a>
                                    <!-- <a href="http://bootstrap-ecommerce.com/developer.html#" class="btn  btn-outline-primary"> <span class="text">Add to cart</span> <i class="fas fa-shopping-cart"></i>  </a> -->
                                </article>
                                <!-- product-info-aside .// -->
                            </main>
                            <!-- col.// -->
                        </div>
                        <!-- row.// -->
                    </div>
                    <!-- card.// -->
                </output>
            </div>
        </section>

    </div>

</template>
<script>
	import axios from 'axios';

export default {
    data(){
        return{
				baseUrl:'http://localhost:3000',
        productId:this.$route.params.productId,

            product:''
        }
    },
		mounted(){
			axios.get(`${this.baseUrl}/products/${this.productId}`)
			.then(response =>{
				this.product = response.data;
				console.log(response.data);
			})
			.catch( (error) =>{
				// handle error
				console.log(error);
			})
		}

}
</script>

<style scoped>

.gallery-wrap .img-big-wrap {
    margin-bottom: 10px;
    border-radius: 0.37rem;
    overflow: hidden;
    background-color: #fff;
}
.gallery-wrap .img-big-wrap a {
    text-align: center;
    display: block;
}
.gallery-wrap .thumbs-wrap {
    text-align: center;
}
*, *::before, *::after {
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
}

.gallery-wrap .thumbs-wrap .item-thumb {
    width: 60px;
    height: 60px;
    border: 1px solid #ddd;
    border-radius: 6px;
    margin: 3px;
    display: inline-block;
    overflow: hidden;
}
.gallery-wrap .img-big-wrap img {
    height: 460px;
    width: auto;
    display: inline-block;
    cursor: -webkit-zoom-in;
    cursor: zoom-in;
}
.input-spinner {
    width: 120px;
    -ms-flex-wrap: nowrap;
    flex-wrap: nowrap;
    display: -webkit-inline-box;
    display: -ms-inline-flexbox;
    display: inline-flex;
}

.input-spinner .btn {
    width: 36px;
    text-align: center;
}
.btn-light {
    background-color: #fff;
    border-color: #e4e4e4;
}



</style>
