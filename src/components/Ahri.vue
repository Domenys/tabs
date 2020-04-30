<template>
  <div class="ahri">
    <div 
      class="heroes-skills-box"
      v-for="(ahri, key) in ahriSkills"
      :key="key"
    >
      <span class="skills-name">{{ ahri.name }}</span>
      <span class="skills-type">{{ ahri.type }}</span>
      <img :src="ahri.image" :alt="ahri.name">
    </div>
  </div>
</template>

<script>


export default {
  name: 'Ahri',
  components: {
    
  },
  data: () => ({
    ahriSkills: [
          {
            name: 'Vastayan Grace',
            type: 'passive',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/5/54/Vastayan_Grace.png/revision/latest?cb=20180417183036'
          },
          {
            name: 'Orb of Deception',
            type: 'active',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/1/19/Orb_of_Deception.png/revision/latest?cb=20130929122633'
          },
          {
            name: 'Fox-Fire',
            type: 'active',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/a/a8/Fox-Fire.png/revision/latest?cb=20130929122632'
          },
          {
            name: 'Charm',
            type: 'active',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/0/04/Charm.png/revision/latest?cb=20130929122630'
          },
          {
            name: 'Spirit Rush',
            type: 'ult',
            image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/8/86/Spirit_Rush.png/revision/latest?cb=20130929122634'
          }
        ]
  })
}
</script>

<style lang="less">

</style>