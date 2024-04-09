<script setup>
import Button from "primevue/button";
import Card from "primevue/card";
import Checkbox from "primevue/checkbox";

</script>

<template>
    <div class="loginPanel">
        <img src="../assets/images/logo-danzo.png" alt="logo" class="logo">
        <Card class="center" style="width: 25rem; padding: 40px ;">
            <template #title>Sign in to continue</template>
            <template #subtitle>Enter your email & password to login</template>
            <template #content>
                <form class="flex flex-col gap-5" @submit.prevent>
                    <div>
                        <label for="email">Email address</label>                
                        <input type="email" placeholder="example@gmail.com" name="email" class="px-3 py-2 border border-solid border-black rounded-md">
                    </div>
                    <div>
                        <label for="password">Password</label>
                        <input type="password" placeholder="Password" name="password" class="px-3 py-2 border border-solid border-black rounded-md">
                    </div>
                    <div class="flex justify-between">
                        <div>
                            <input type="checkbox" id="remember" name="remember" style="outline: none; width: min-content;">
                            <label for="remember" class="ml-2"> Remember me </label>    
                        </div>
                        <a href="#" class="text-blue-600">Forgot Password?</a>
                    </div>
                    <Button type="submit" label="Sign in" class="w-full bg-blue-500 text-white p-[10px]"  />
                </form>  
                <div class="flex gap-5 flex-col items-center">
                    <p class="text-gray-500 block   ">Or sign in with</p>
                    <span class="p-buttonset flex gap-3">
                        <Button label="Save" raised icon="pi pi-facebook" />
                        <Button label="Delete" raised icon="pi pi-twitter" />
                        <Button label="Cancel" raised icon="pi pi-linkedin" />
                    </span>
                    <p class="text-gray-500">Don't have account? <span><a href="#" class="text-blue-500">Create Account</a></span> </p>
                </div>
            </template>
        </Card>
    </div>
</template>

<style scoped>
.loginPanel{
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    gap: 20px;
    justify-content: center;
    align-items: center;
    background: url("../assets/images/coming-soon-bg.jpg") no-repeat center/cover;
}
input{
    background: rgba(48, 126, 243, 0.1);
    outline: none;
    border: rgba(48, 126, 243, 0.6);
    width: 100%;
}
input:focus{
    outline: 1px solid rgba(48, 126, 243, 1);
}

.p-buttonset{
    display: flex;
    justify-content: space-between;
}

.p-buttonset button{
    padding: 10px 20px;
}
</style>