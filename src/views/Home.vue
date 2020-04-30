<template>
  <div class="home">
    <div class="heroes-info">
      <div 
        class="heroes-box"
        v-for="(hero, key) in tabs"
        :key="key"
        v-on:click="currentHero = hero"
      >
        <span class="hero-name">{{ hero.name }}</span>
        <img :src="hero.image" :alt="hero.name">
      </div>
    </div>
    <div class="heroes-skills-info">
      <component :is="currentHero.component" class="tab"></component>
    </div>
  </div>
</template>

<script>
import Nasus from '@/components/Nasus'
import Ahri from '@/components/Ahri'
import Azir from '@/components/Azir'
import Nidalee from '@/components/Nidalee'

let tabs = [
        {
          name: "Nasus",
          image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/b/bf/Nasus_Render.png/revision/latest/scale-to-width-down/350?cb=20190119234048',
          component: Nasus
        },
        {
          name: "Ahri",
          image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/f/f1/Ahri_Render.png/revision/latest/scale-to-width-down/350?cb=20200328135939',
          component: Ahri
        },
        {
          name: "Azir",
          image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/d/d6/Azir_Render.png/revision/latest/scale-to-width-down/350?cb=20181110231930',
          component: Azir
        },
        {
          name: "Nidalee",
          image: 'https://vignette.wikia.nocookie.net/leagueoflegends/images/0/00/Nidalee_Render.png/revision/latest/scale-to-width-down/243?cb=20181117195625',
          component: Nidalee
        }
      ]

export default {
  name: 'Home',
  components: {
    Nasus,
    Ahri,
    Azir,
    Nidalee
  },
  data: () => ({
    tabs: tabs,
    currentHero: tabs[0]
  })
}
</script>

<style lang="less">
  img {
    width: 100px;
    height: 100px;
    box-shadow: inset 0px 0px 73px 2px rgba(0,0,0,0.51);
    margin-right: 5px;
    border-radius: 25px;
  }
  .heroes-info {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    .heroes-box {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
  }
  .nasus,
  .ahri,
  .azir,
  .nidalee {
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        align-items: center;
        margin-bottom: 10px;
        .heroes-skills-box {
            display: flex;
            flex-direction: column;
            justify-content: space-around;
            align-items: center;
            flex: 1 0 20%;
        }
    }
</style>