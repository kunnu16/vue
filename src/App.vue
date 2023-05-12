<template>
  <header>
    <!-- <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="This is the first application of Vue Js" />
    </div>
      <HomeVue />
      <HomeVue /> -->
      <CounterVue/>
  
  </header>
  
</template>

<script>
import CounterVue from './components/Counter.vue';
// import HelloWorld from './components/HelloWorld.vue';
import HomeVue from './components/Home.vue';


export default {
  name : "App",
  components : {
    // HelloWorld,
    // HomeVue,
    CounterVue
  }
}
</script>>
<!-- <style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>  -->
