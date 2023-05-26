<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <!-- <div class="wrapper">
      <HelloWorld msg="This is the first application of Vue Js" />
    </div> -->
      <!-- <HomeVue /> -->
      <!-- <HomeVue /> -->
      <!-- <CounterVue/> -->
      <!-- <HomeVue /> -->
      <!-- <ParentVue /> -->
      <!-- <ClassBindingVue /> -->
      <!-- <ModifiersVue /> -->
      <!-- <TodoAppVue /> -->
      <!-- <WatchersVue /> -->
      <!-- <SlotsVue /> -->
      <!-- <DynamicVue /> -->
      <!-- <TeleportVue /> -->
      <!-- <CreatedVue /> -->
      <!-- <MountVue /> -->
      <!-- <UpdateVue /> -->


      <!-- <Ref_ReactiveVue /> -->
      <!-- <watcherVue /> -->
      <TemplateRefVue />
  </header>
  
</template>

<script>
import ClassBindingVue from './components/ClassBinding.vue';
import CounterVue from './components/Counter.vue';
import CreatedVue from './components/Created.vue';
import DynamicVue from './components/Dynamic.vue';
import HelloWorld from './components/HelloWorld.vue';
import HomeVue from './components/Home.vue';
import ModifiersVue from './components/Modifiers.vue';
import MountVue from './components/Mount.vue';
import ParentVue from './components/Parent.vue';
import Ref_ReactiveVue from './components/Ref_Reactive.vue';
import SlotsVue from './components/Slots.vue';
import TeleportVue from './components/Teleport.vue';
import TemplateRefVue from './components/TemplateRef.vue';
import TodoAppVue from './components/TodoApp.vue';
import UpdateVue from './components/Update.vue';
import watcherVue from './components/watcher.vue';
import WatchersVue from './components/Watchers.vue';

export default {
  name : "App",
  components : {
    HelloWorld,
    HomeVue,
    CounterVue,
    HomeVue,
    ParentVue,
    ClassBindingVue,
    ModifiersVue,
    TodoAppVue,
    WatchersVue,
    SlotsVue,
    DynamicVue,
    TeleportVue,
    CreatedVue,
    MountVue,
    UpdateVue,

    // composition API
    Ref_ReactiveVue,
    watcherVue,
    TemplateRefVue
    
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
