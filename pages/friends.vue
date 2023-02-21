<template>
  <b-card
    img-src="https://upload.wikimedia.org/wikipedia/commons/9/91/Beat_Saber_Logo.png"
    :title="title"
    img-alt="https://upload.wikimedia.org/wikipedia/commons/9/91/Beat_Saber_Logo.png"
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
      title: 'Add a Friend'
    }
  },
  methods: {
    clickOnMe () {
      this.title = 'Unknown'
    }
  }
}
</script>
