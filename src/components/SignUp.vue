<template>
    <h1>Sign Up</h1>
    <div class="signup">
        <input type="text" placeholder="Enter Name"/>
        <input type="text" placeholder="Enter Email"/>
        <input type="password" placeholder="Enter Password"/>
        <button>Sign Up</button>
    </div>
</template>
<script>
export default {
    name: 'SignUp'
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
}
</style>