<template>
  <div id="app">
    <HeaderMain></HeaderMain>
    <About></About>
    <Skills></Skills>
    <Portfolio></Portfolio>
    <Contacts></Contacts>
  </div>
</template>

<script>

import HeaderMain from "./components/HeaderMain";
import About from "./components/About";
import Skills from "./components/Skills";
import Portfolio from "./components/Portfolio";
import Contacts from "./components/Contacts";

export default {
  name: 'App',
  components: {
    HeaderMain,
    About,
    Skills,
    Portfolio,
    Contacts,
  }
}
</script>

<style lang="scss">

</style>
