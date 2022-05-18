<template>
  <q-page padding>
    <div class="q-pa-md row items-stretch">

      <plat v-for="p in plats"
            :key="p.id"
            :passeplat="p"
            @supprimer="supprimerPlat"
      ></plat>

    </div>
  </q-page>n
</template>

<script>
export default {
  components: {
    plat: require('components/PlatComp.vue').default
  },
  data () {
    return {
      plats: [
        {
          id: 23,
          image: 'https://i.imgur.com/0umadnY.jpg',
          nom: 'Burger',
          description: "Un hamburger est un sandwich composé d'une ou plusieurs tranches de viande hachée, généralement du bœuf, placées dans un petit pain ou une brioche.",
          note: 4
        },
        {
          id: 2,
          image: 'https://i.imgur.com/b9zDbyb.jpg',
          nom: 'Pizza',
          description: "La pizza est un plat savoureux d'origine italienne, consistant en une base généralement ronde et aplatie de pâte levée à base de blé.",
          note: 5
        },
        {
          id: 8,
          image: 'https://i.imgur.com/0umadnY.jpg',
          nom: 'Burger',
          description: "Un hamburger est un sandwich composé d'une ou plusieurs tranches de viande hachée, généralement du bœuf, placées dans un petit pain ou une brioche.",
          note: 1
        },
        {
          id: 54,
          image: 'https://i.imgur.com/xAuhNVg.jpg',
          nom: 'BBQ Ris',
          description: 'Les BBQ ribs ou barbecue ribs sont des grands classiques très appréciés partout dans le monde.',
          note: 5
        }
      ]
    }
  },
  methods: {
    supprimerPlat (idPlatASupprimer) {
      this.plats = this.plats.filter(function (plat) {
        return plat.id !== idPlatASupprimer
      })
    }
  }
}
</script>
