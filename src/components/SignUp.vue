<template>
    <h1>Sign Up</h1>
    <div class="signup">
        <input type="text" v-model="name" placeholder="Enter Name"/>
        <input type="text" v-model="email" placeholder="Enter Email"/>
        <input type="password" v-model="password" placeholder="Enter Password"/>
        <button v-on:click="signUp">Sign Up</button>
    </div>
</template>
<script>
import axios from 'axios'
export default {
    name: 'SignUp', 
    data () {
        return {
            name: '',
            email: '',
            password: ''
        }
    }, 
    methods: {
        async signUp()
        {
            let result = await axios.post("http://localhost:3000/users", 
            {
                name:this.name, 
                email:this.email,
                password:this.password
            });
        console.warn(result);
        if(result.status==201)
        {
           
            localStorage.setItem("user-info",JSON.stringify(result.data))
            this.$router.push({name:"Home"})
        }
        }
    }, 
    mounted() 
    {
        let user = localStorage.getItem('user-info');
    if(user)
    {
        this.$router.push({name:"Home"})
    }}
}
</script>
<style>

.signup input{
width: 300px;
height: 30px;
display: block;
margin: auto;
margin-bottom: 30px;
padding-left: 10px;
border: 1px solid darkblue;
}
.signup button {
width: 300px;
height: 30px;
border: 1px solid darkblue;
border-radius: 8px 0px;
background-color: darkblue;
color: white;
cursor: pointer;
}
</style>