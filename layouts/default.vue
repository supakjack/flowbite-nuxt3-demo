<template>
    <div>
        <NuxtLink :to="{name:'index'}">Home page</NuxtLink>
        <NuxtLink :to="{name:'about'}">About page</NuxtLink>
        <slot />
    </div>
</template>