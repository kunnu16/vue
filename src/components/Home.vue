<template>
<div>
    <!-- <h1 v-on:mousemove="getConsole">Hello from Home components...</h1>
    <h1>Name :{{Name}}</h1>
    <h1>Mobile :{{getMobile()}}</h1>
    <h1>getEmail :{{getEmail("kp@xyz.com")}}</h1>
    <h1>Name : {{Name}}</h1>
    <input type="text" v-model="count" />
    <h1>{{count}}</h1> -->



    <h1>get Input field Data</h1>
    <input v-if="state === true" type="text" placeholder="enter your emailId" v-model="email" />
    <br /><br />
    <input v-if="state === true" type="text" placeholder="enter your Password" v-model="password" />
    <br /><br />
    <p>{{characterCount}}/20</p>
    <button v-on:click="getData()">get Data</button>
    <!-- <button @click="users.push({email ,password})">get Data</button> -->
    <button @click="state = !state">Change State</button>
    <button v-bind:disabled="email === '' || password === '' "  @click="saveData()">Add Data</button>
    
    <!-- <a :href="email">dynamic Link</a> -->
    
    <h1 v-if="users.length === 0">There is no user in users array</h1>
    <h1 v-for="user in users" :key="user.email">{{user}}</h1>

    <h1>{{email}} and {{password}}</h1>
    
    <h1 v-for="ticket in tickets" :class="{strikeout: ticket.buy}" :key="ticket.buy" >{{ticket.label}}</h1> 
     <!-- <h1 v-for="ticket in tickets" :class="[ticket.buy ? 'strikeout' : '' , ticket.high ? 'priority' : '' ]"  :key="ticket.buy" >{{ticket.label}}</h1>  -->

    <!-- <h1>Technologies</h1>
    <label for="C++">C++</label>
    <input type="checkbox" value="C++" id="C++" v-model="technology" />

    <label for="Vue">Vue</label>
    <input type="checkbox" value="Vue" id="Vue" v-model="technology"/>

    <label for="Node">Node</label>
    <input type="checkbox" value="Node" id="Node" v-model="technology"/>

    <br/>
    <h2>Technology : {{technology}}</h2>
    <br/><br/>

    <h1>who i am</h1>
    <label for="student">Student</label>
    <input type="radio" value="student" name="who" id="student" v-model="who"/>

    <label for="developer">Developer</label>
    <input type="radio" value="developer" name="who" id="developer" v-model="who"/>

    <br/>
    <h2>I am a : {{who}}</h2>
    <br/><br/> -->

    <!-- <h1 v-if="show">if condition</h1>
    <h1 v-else>else condition</h1>
    <button v-on:click="show=!show">toggle</button> -->

    <!-- <ul>
        <li v-for="tech in technologies" :key="tech">
            {{tech}}
        </li>
    </ul>
    <br /><br />

    <ul>
        <li v-for="userInfo in User" :key="userInfo.email">
            Name is {{userInfo.Name}} and EmailId is {{userInfo.email}}
        </li>
    </ul> -->

</div>
</template>

<script>
export default {
    name: 'Home',
    data() {
        return {
            // Name: "Kunal Parmar",
            // Mob: 123445,
            // Email: "kp@xyz.com",
            // count:10,

            users : [],
            email:'',
            password:'',
            state:true,
            
            tickets : [{
                label : 'Football',
                buy : false,
                high : false
            },
            {
                label : 'Cricket',
                buy : true,
                high:false,
            },{
                label : 'Chess',
                buy : false,
                high:false
            }],

            
            // technology:[],
            // who:null,

            // show : true,

            // technologies: ["C++", "Javascript", "Node", "Vue"],
            // User: [{
            //         Name: "Kunal",
            //         email: "kunal@parmar.com"
            //     },
            //     {
            //         Name: "Nitik",
            //         email: "nitik@patidar.com"
            //     }, {
            //         Name: "NSA",
            //         email: "ns@anjana.com"
            //     }
            // ]
        }
    },
    computed: {
        characterCount() {
            return this.password.length;
        }
    },
    methods: {
        // getEmail(email) {
        //     return email;
        // },
        // getMobile() {
        //     return this.Mob;
        // },
        // getConsole() {
        //     console.log("getConsole Called!");
        // },
        getData() {
            console.log("Input Field value : " , this.email ,this.password);
            this.email = "";
            this.password = "";
        },
        saveData() {
            this.users.push({email:this.email ,password:this.password}),
            this.email = "";
            this.password = "";
        }
    }
}
</script>

<style scoped>
h1 {
    color: rgb(59, 57, 57);
}
</style>
