<template>
<div>
  <b-card :title="book.title"
          img-src="https://www.thelakeviewhusky.com/wp-content/uploads/2018/11/dgdzhbdbnghqvvogxw8biu7o_21.jpg"
          img-alt="Image"
          img-top
          tag="article"
          style="max-width: 20rem;"
          class="mb-2">
    <p class="card-text">
      {{book.subtitle}}
    </p>
    <b-button href="#" variant="primary">Go somewhere</b-button>
  </b-card>
</div>
</template>

<script>
export default {
    props: ['book']
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
