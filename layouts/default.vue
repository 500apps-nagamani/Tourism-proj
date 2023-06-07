<script setup lang='ts'>

</script>

<template>
    <div>
        <header>
            <nav>
                <ul>
                    <li>
                        <NuxtLink to="/"> Home </NuxtLink>
                        <NuxtLink to="/places"> Places </NuxtLink>
                    </li>
                </ul>
            </nav>
        </header>
        <slot />
    </div>
</template>

<style lang="scss" scoped>

</style>