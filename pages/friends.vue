<template>
  <b-row class="mt-4">
    <b-col cols="4" class="mb-4">
      <b-card
        img-src="https://upload.wikimedia.org/wikipedia/commons/9/91/Beat_Saber_Logo.png"
        :title="title"
        img-alt="https://upload.wikimedia.org/wikipedia/commons/9/91/Beat_Saber_Logo.png"
        img-top
        tag="article"
        class="mb-2"
        bg-variant="dark"
        text-variant="white"
      >
        <b-card-body>
          You can easy add friend to this hall
        </b-card-body>

        <b-card-footer>
          <b-input v-model="idToAdd" />
          <b-button href="#" variant="primary" :disabled="!idToAdd" @click="clickOnMe">
            Add a friend!
          </b-button>
        </b-card-footer>
      </b-card>
    </b-col>

    <b-col
      v-for="(friend, i) in friends"
      :key="i"
      cols="4"
      class="mb-4"
    >
      <b-card
        :img-src="friend.avatar"
        :title="friend.playerName"
      >
        <b-card-body>
          PP: {{ friend.pp }}<br>
          countryRank: {{ friend.countryRank }}<br>
          rank: {{ friend.rank }}
        </b-card-body>
      </b-card>
    </b-col>
  </b-row>
</template>

<script>
export default {
  name: 'TestPage',
  data () {
    return {
      title: 'Add a Friend',
      idToAdd: '76561198202677324',
      friends: []
    }
  },
  methods: {
    clickOnMe () {
      fetch('https://new.scoresaber.com/api/player/' + this.idToAdd + '/full').then(
        async (Response) => {
          const data = await Response.json()

          if (data.playerInfo) {
            const friend = {
              playerName: data.playerInfo.playerName,
              avatar: 'https://new.scoresaber.com' + data.playerInfo.avatar,
              rank: data.playerInfo.rank,
              countryRank: data.playerInfo.countryRank,
              pp: data.playerInfo.pp
            }
            this.friends.push(friend)
          }
        }
      )
    }
  }
}
</script>
