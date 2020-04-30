<template>
  <div class="nasus">
    <div 
        class="heroes-skills-box"
        v-for="(nasus, key) in nasusSkills"
        :key="key"
    >
        <span class="skills-name">{{ nasus.name }}</span>
        <span class="skills-type">{{ nasus.type }}</span>
        <img :src="nasus.image" :alt="nasus.name">
    </div>
  </div>
</template>

<script>


export default {
  name: 'Nasus',
  components: {
    
  },
  data: () => ({
      nasusSkills: [
          {
            name: 'Soul Eater',
            type: 'passive',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/6/6c/Soul_Eater.png/revision/latest?cb=20170818192444'
          },
          {
            name: 'Siphoning Strike',
            type: 'active',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/9/9e/Siphoning_Strike.png/revision/latest?cb=20170818192422'
          },
          {
            name: 'Wither',
            type: 'active',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/a/aa/Wither.png/revision/latest?cb=20170818192532'
          },
          {
            name: 'Spirit Fire',
            type: 'active',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/9/9b/Spirit_Fire.png/revision/latest?cb=20170818192458'
          },
          {
            name: 'Fury of the Sands',
            type: 'ult',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/0/01/Fury_of_the_Sands.png/revision/latest?cb=20170818192359'
          }
        ]
  })
}
</script>

<style lang="less">
    
</style>