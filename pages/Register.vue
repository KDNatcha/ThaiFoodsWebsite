<template>
    <div class="flex min-h-full flex-col justify-center px-6 py-12 lg:px-8">
      
        <nuxt-link to="./">index</nuxt-link>
        <div class="sm:mx-auto sm:w-full sm-max-w-sm">
        <h1 class="mt-10 text-center text-2xl font-bold "> Register</h1>
        <div class="mt-10 sm:mx-auto sm:w-full sm:max-w-sm">
        <form class="space-y-6" action="" method="post">
            <label for="username" class="block text-sm font-medium leading-6 ">Username:</label>
            <input id="username" v-model="username" type="text" maxlength="20" required class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset sm:text-sm sm:leading-6">
        
        <label for="email" class="block text-sm font-medium leading-6 ">Email:</label>
        <input id="email" v-model="email" type="email" required class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset sm:text-sm sm:leading-6"> 
        
        <label for="password" class="block text-sm font-medium leading-6 ">Password:</label>
        <input id="password" v-model="password" type="password" required class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset sm:text-sm sm:leading-6">

        <label for="confirmpassword" class="block text-sm font-medium leading-6 ">Confirm Password:</label>
        <input id="confirmpassword" v-model="confirmpassword" type="password" required class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset sm:text-sm sm:leading-6">
        
        <button type="submit" class="flex w-full justify-center rounded-md">Register</button>
        </form>
    </div>
    </div>
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
      async register() { 
        //const { data } = await axios.get()
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
    
</style>