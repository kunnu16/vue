<template>
  <div>
    <!-- <h1>Slot component</h1> -->
    <!-- <SlotChildVue> <h1>Kunal Parmar</h1></SlotChildVue>
    <SlotChildVue> <a href="#">vueSchool.com</a></SlotChildVue>
    <SlotChildVue> <h1>Kunal Parmar</h1></SlotChildVue>
    <SlotChildVue></SlotChildVue> -->

    <SlotChildVue>
      <template v-slot:header>
        <h1>Gammastack</h1>
      </template>

      <template v-slot:main>
        <p>Casino</p>
      </template>

      <template v-slot:footer>
        <button>Play</button>
      </template>
    </SlotChildVue>

    <SlotChildVue>
      <template v-slot:header>
        <h1>Grepruby</h1>
      </template>

      <template v-slot:main>
        <p>MERN</p>
      </template>

      <template v-slot:footer>
        <button>Play</button>
      </template>
    </SlotChildVue>
  </div>
</template>

<script>
import SlotChildVue from "./SlotChild.vue";

export default {
  name: "Slots",
  components: {
    SlotChildVue,
  },
};
</script>

<style>
</style>
