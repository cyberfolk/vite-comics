<script>
import dc_comicss from "../data/dc-comics.json";
import ProductItem from "./ProductItem.vue";

export default {
  name: "ProductList",
  components: {
    ProductItem,
  },
  data() {
    return {
      dc_comicss: dc_comicss,
    };
  },
};
</script>

<template>
  <div class="container">
    <div class="row row-cols-2 row-cols-lg-6 g-2 g-lg-3 py-5">
      <ProductItem :src="comic.thumb" :title="comic.series" v-for="comic in dc_comicss" />
    </div>
  </div>
  <!-- /.container -->
</template>
