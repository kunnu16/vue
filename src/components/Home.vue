<template>
<h1>Hello from Home components...</h1>
<h1>Name {{Name}}</h1>
<h1>Mobile {{getMob()}}</h1>
<h1>getEmail {{getEmail('kp@xyz.com')}}</h1>
</template>

<script>
export default {
    name: 'Home',
    data() {
        return {
            Name: "Kunal Parmar",
            Mob: 123445,
            Email: "kp@xyz.com"
        }
    },
    methods : {
        getEmail(email) {
            return email;
        },
        getMobile() {
            return this.Mob;
        }
    }
}
</script>

<style scoped>
h1 {
    color: red;
}
</style>
