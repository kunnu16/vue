<template>
  <div>
    <!-- <slot><h2>Gammastack</h2></slot> -->


    
    <header>
      <slot name="header"></slot>
    </header>

    <content>
      <slot name="main"></slot>
    </content>

    <footer>
      <slot name="footer"></slot>
    </footer>
  </div>
</template>

<script>
export default {
  name: "SlotChild",
};
</script>

<style>
</style>