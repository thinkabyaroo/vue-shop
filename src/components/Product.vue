<template>
  <div class="col-6 col-md-4 col-xl-3">
      <div class="card">
        <div class="card-body">
          <figure>
            <img :src="productDetail.image" class="product-img" alt="">
          </figure>
          <p>{{productDetail.title}}</p>

          <div class="d-flex justify-content-between">
            <p>${{productDetail.price}}</p>
              <Rating :rating="productDetail.rating"></Rating>
          </div>
          <button class="btn btn-outline-dark w-100">Add to cart</button>
        </div>
      </div>
  </div>
</template>

<script>
import Rating from "@/components/Rating";
export default {
  components: {Rating},
  props: ["productDetail"],
}
</script>

<style >
.product-img{
  height: 100px;
  width: 100px;
}

</style>