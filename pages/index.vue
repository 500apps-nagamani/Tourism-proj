



<template>
    <div class="main flex flex-col justify-end">

        
        <div class="bg-white p-3 rounded-md">
            <h1 class="text-2xl font-bold italic font-serif">Tourism</h1>
            <p class="italic text-lg">Plan your trip wherever you want to go</p>
            <NuxtLink to="/places">
                <button class="btn mt-4">Get started</button>
            </NuxtLink>
        </div>
    </div>
</template>


<script setup>




</script>


<style scoped>
.main{
    background-image: url("https://images.theconversation.com/files/295442/original/file-20191003-52796-1763ajl.jpg?ixlib=rb-1.1.0&q=45&auto=format&w=1200&h=900.0&fit=crop");
    height : 90vh;
    background-size: cover;
}
</style>
