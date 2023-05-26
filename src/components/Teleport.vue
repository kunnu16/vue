<template>
  <div>
    <h1>Teleport Component</h1>

    <teleport to="#Footer">
        <FooterVue />
    </teleport>
  
  </div>
</template>

<script>
import FooterVue from './Footer.vue'

export default {
    name : 'Teleport',
    components : {
        FooterVue,
    }
}
</script>

<style>

</style>