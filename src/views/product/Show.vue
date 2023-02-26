<template>
</template>

<script>
export default {
  name: "Index.vue",
  mounted() {
    $(document).trigger('init')
    this.getProduct()
  },

  data() {
    return {
      products: []
    }
  },

  methods: {

    getProduct() {
      this.axios.get('http://localhost:8876/api/products/'${id})
          .then(res => {
            console.log(res.data.data);
            this.products = res.data.data;
          })
          .finally( v => {
            $(document).trigger('init')
          })
    }
  }

}
</script>

<style scoped>

</style>