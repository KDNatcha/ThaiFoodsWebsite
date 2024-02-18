<template>
    <div>
      
        <nuxt-link to="./">index</nuxt-link>

        <h1> Register</h1>
        <form @submit.prevent="register" method="post">
            <label for="username">Username:</label>
        <input id="username" v-model="username" type="text">
        
        <label for="email">Email:</label>
        <input id="email" v-model="email" type="email">
        
        <label for="password">Password:</label>
        <input id="password" v-model="password" type="password">
        <label for="confirmpassword">Confirm Password:</label>
        <input id="confirmpassword" v-model="password" type="password">
        <button type="submit">Register</button>
        </form>
    </div>
</template>
<script>
export default{
    data(){
        return{
            username:'',
            email: '',
            password: '',
            confirmpassword:'',
        };
    },
    methods: {
      register() {
        if (this.password !== this.confirmPassword) {
        alert('Passwords do not match');
        return;
      }
        // Handle registration logic here
        console.log('Registering user...');
        console.log('Username:', this.username);
        console.log('Email:', this.email);
        console.log('Password:', this.password);

      }
    }
};
</script>
<style>
h1{
    text-align: center;
    
}
input{
    border: solid 1px black;
    border-radius: 5px;
    margin: 5px;
    white-space: pre-line;
}
    input[type=button],
    input[type=submit]{
    background-color: black;
    color: white;
    padding: 10px;  
    
}
</style>