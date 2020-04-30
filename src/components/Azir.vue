<template>
  <div class="azir">
    <div 
        class="heroes-skills-box"
        v-for="(azir, key) in azirSkills"
        :key="key"
    >
        <span class="skills-name">{{ azir.name }}</span>
        <span class="skills-type">{{ azir.type }}</span>
        <img :src="azir.image" :alt="azir.name">
    </div>
  </div>
</template>

<script>


export default {
  name: 'Azir',
  components: {
    
  },
  data: () => ({
    azirSkills: [
          {
            name: 'Shurima\'s Legacy',
            type: 'passive',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/4/4f/Shurima%27s_Legacy.png/revision/latest?cb=20170818001505'
          },
          {
            name: 'Conquering Sands',
            type: 'active',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/8/87/Conquering_Sands.png/revision/latest?cb=20170818001434'
          },
          {
            name: 'Arise!',
            type: 'active',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/6/61/Arise%21.png/revision/latest?cb=20171201215426'
          },
          {
            name: 'Shifting Sands',
            type: 'active',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/7/7f/Shifting_Sands.png/revision/latest?cb=20180522191603'
          },
          {
            name: 'Emperor\'s Divide',
            type: 'ult',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/2/21/Emperor%27s_Divide.png/revision/latest?cb=20170818001445'
          }
        ]
  })
}
</script>

<style lang="less">

</style>