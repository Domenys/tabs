<template>
  <div class="nidalee">
    <div 
        class="heroes-skills-box"
        v-for="(nidalee, key) in nidaleeSkills"
        :key="key"
    >
        <span class="skills-name">{{ nidalee.name }}</span>
        <span class="skills-type">{{ nidalee.type }}</span>
        <img :src="nidalee.image" :alt="nidalee.name">
    </div>
  </div>
</template>

<script>


export default {
  name: 'Nidalee',
  components: {
    
  },
  data: () => ({
    nidaleeSkills: [
          {
            name: 'Prowl',
            type: 'passive',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/4/4f/Prowl.png/revision/latest?cb=20140627151211'
          },
          {
            name: 'Javelin Toss',
            type: 'active',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/d/d3/Javelin_Toss.png/revision/latest?cb=20160608032959'
          },
          {
            name: 'Bushwhack',
            type: 'active',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/5/5f/Bushwhack.png/revision/latest?cb=20160608032938'
          },
          {
            name: 'Primal Surge',
            type: 'active',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/3/3f/Primal_Surge.png/revision/latest?cb=20140627151506'
          },
          {
            name: 'Aspect of the Cougar',
            type: 'ult',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/2/21/Aspect_of_the_Cougar.png/revision/latest?cb=20160608032916'
          }
        ]
  })
}
</script>

<style lang="less">

</style>