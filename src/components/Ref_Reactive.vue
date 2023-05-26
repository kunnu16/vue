<template>
<div>
    <!-- <h1>{{count}}</h1>
    <button @click="increment()">click</button> -->

    <h1>{{state.count}}</h1>
    <button @click="increment()">click</button>

    <!-- <h2>{{user.Age}}</h2> -->
    <h2>{{Age}}</h2>
</div>
</template>

<script>
import {isReactive, isRef,reactive,ref,toRefs} from 'vue';

export default {
    setup() {
        // const count = ref(0);

        // function increment() {
        //     count.value++;
        // }

        const state = reactive({
            count: 0
        });

        const user = reactive({
            userName : 'Nitik',
            Age : 21,
            email : 'nikki@abc.com'
        })
        function increment() {
            state.count++
        }

        console.log(isReactive(state));
        return {
            // count,
            // increment,

            state,
            increment,
            // user,
            ...toRefs(user)
        }
    }
}
</script>

<style>

</style>
