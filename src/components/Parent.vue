<template>
<div>
    <!-- <h1>Pass data from parent to child</h1>
    <ChildVue name="Kunal Parmar" :userInfo="user" :getData="getData" /> -->

    <ul>
        <li v-for="item in users" :key="item.name">
            <UserVue :data="item" :getName="getName"/>
        </li>
    </ul>

</div>
</template>

<script>
import ChildVue from './Child.vue'
import UserVue from './User.vue'

export default {
    name: "Parent",
    components: {
        ChildVue,
        UserVue
    },
    data() {
        return {
            // user : {userId : "NSA" , email:"ns@anjana.com"},

            users: [{
                    name: "Kunal",
                    email: "kp@abc.com"
                },
                {
                    name: "Aman",
                    email: "am@abc.com"
                },
                {
                    name: "Nitik",
                    email: "np@abc.com"
                },
                {
                    name: "Ankit",
                    email: "ag@abc.com"
                }
            ]
        }
    },
    methods: {
        // getData() {
        //     console.log("getData Function Called!"); 
        //     alert("getData function called!!!")
        // },
        getName(name) {
            console.log(name);
            alert(name);
        }
    }
}
</script>

<style scoped>
h1 {
    color: rgb(243, 128, 13);
}
</style>
