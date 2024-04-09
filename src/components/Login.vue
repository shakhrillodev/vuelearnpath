<script setup>
import Button from "primevue/button";
import Card from "primevue/card";
import Checkbox from "primevue/checkbox";

</script>

<template>
    <Card class="center" style="width: 25rem; overflow: hidden; padding: 20px ;">
        <template #title>Sign in to continue</template>
        <template #subtitle>Enter your email & password to login</template>
        <template #content>
            <form class="flex flex-col gap-3">
                <label for="email">Your email</label>                
                <input type="email" placeholder="example@gmail.com" name="email" class="px-3 py-2 border border-solid border-black rounded-md">
                <label for="password">Password</label>
                <input type="password" placeholder="Password" name="password" class="px-3 py-2 border border-solid border-black rounded-md">
                <Button label="Sign in" class="w-full bg-blue-800 text-white p-[10px]"  />
            </form>  
        </template>
    </Card>
</template>

<style scoped>
</style>