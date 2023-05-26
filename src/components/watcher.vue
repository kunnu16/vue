<template>
  <div>
    <h1>{{ user }}</h1>
    <h1>{{ user2 }}</h1>
    <button @click="user = 'Nikki'">change</button>
    <button @click="user2 = 'jklo'">change2</button>
    <br />
    <input type="text" placeholder="student name" v-model="student.name" />
    <br />
    <br />
    <input type="text" placeholder="address" v-model="student.address.city" />

    <h1>{{ student.name }}</h1>
  </div>
</template>

<script>
import { reactive, ref, watch } from "vue";

export default {
  setup() {
    const user = ref("Nitik");
    const user2 = ref("abcd");

    const student = reactive({
      name: "Ankit",
      age: "22",
      email: "ak@xyz.com",
      address: {
        city: "indore",
        pincode: "123",
        dis: "abc",
      },
    });

    // watch(
    //   [user, user2],
    //   (newval, oldval) => {
    //     console.log(newval, oldval);
    //   },
    //   { immediate: true }
    // );

    // watch(() => {
    //   return {...student}
    // } , (newval,oldval) => {
    //   console.log(newval , oldval);
    // })

    // watch(
    //   () => {
    //     return student.name;
    //   },
    //   (newval, oldval) => {
    //     console.log(newval, oldval);
    //   }
    // );

      watch(
      () => {
        return student.address;
      },
      (newval, oldval) => {
        console.log(newval, oldval);
      },{deep:true}
    );

    return {
      user,
      user2,
      student,
    };
  },
};
</script>

<style>
</style>
