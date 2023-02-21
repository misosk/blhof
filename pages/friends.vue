<template>
  <b-card
    img-src="https://upload.wikimedia.org/wikipedia/commons/9/91/Beat_Saber_Logo.png"
    :title="title"
    img-alt="https://upload.wikimedia.org/wikipedia/commons/9/91/Beat_Saber_Logo.png"
    img-top
    tag="article"
    style="max-width: 20rem;"
    class="mb-2"
    bg-variant="dark"
    text-variant="white"
  >
    <b-button href="#" variant="primary" @click="clickOnMe">
      Add a friend!
    </b-button>
  </b-card>
</template>

<script>
function $ (s) {

}

export default {
  name: 'TestPage',
  data () {
    return {
      title: 'Add a Friend'
    }
  },
  methods: {
    clickOnMe () {
      const userName = prompt('Please Input your Scoresaber Profile ID (Number Only)')

      fetch('https://new.scoresaber.com/api/player/' + userName + '/full').then(
        async (Response) => {
          const data = await Response.json()
          console.log(data)
          // eslint-disable-next-line no-unused-expressions
          data.playerInfo.playerName
          $('#playerName').text(data.playerInfo.playerName)
          $('#avatar').attr('src', 'https://new.scoresaber.com' + data.playerInfo.avatar)
          $('#rank').text(data.playerInfo.rank)
          $('#countryRank').text(data.playerInfo.countryRank)
          $('#PP').text(data.playerInfo.pp)
        }
      )
    }
  }
}
</script>
