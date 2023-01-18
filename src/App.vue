<template>

<AppHeader></AppHeader>

<router-view></router-view>
  <!-- other content :herotitle="'blah blah\nblah'"-->
  <AppHero  herotitle="Lorem ipsum dolor sit amet consectetur adipisicing"  subtitle="Lorem ipsum dolor sit amet"  ></AppHero>

  <AppTitle  title="Lorem ipsum dolor sit amet." paragraph="Donec pede justo, fringilla vel, aliquet nec, vulputate eget, Donec pede justo, fringilla vel, aliquet nec, vulputate eget"></AppTitle >

  <AppCta ctatitle="Lorem ipsum dolor sit amet" > </AppCta>


  <AppFooter> </AppFooter> 


</template>

<script>

import AppHeader from './components/AppHeader.vue'
import AppHero from './components/AppHero.vue'
import AppTitle from './components/AppTitle.vue'
import AppCta from './components/AppCta.vue'

import AppFooter from './components/AppFooter.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppHero,
    AppTitle,
    AppCta,
    AppFooter
 
   

}
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}
</style>
