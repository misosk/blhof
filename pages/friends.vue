<template>
  <b-card
    :title="title"
    img-src="https://picsum.photos/600/300/?image=25"
    img-alt="Image"
    img-top
    tag="article"
    style="max-width: 20rem;"
    class="mb-2"
  >
    <b-card-text>
      Ready to start adding friends? Hit the blue button below to add someone!
    </b-card-text>

    <b-button href="#" variant="primary" @click="clickOnMe">
      Add a friend!
    </b-button>
  </b-card>
</template>

<script>
export default {
  name: 'TestPage',
  data () {
    return {
      title: 'hello'
    }
  },
  methods: {
    clickOnMe () {
      this.title = 'how are you'
    }
  }
}
</script>
