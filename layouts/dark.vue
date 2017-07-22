<template>
    <div class="dark">
        <nuxt/>
    </div>
</template>

<style>
    .dark{
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        min-height: 100%;
        padding: 10px;
        color: white;
        background: black;
    }
    .dark a{
        color: green;
    }
    .dark a:hover{
        color: yellow;
    }
</style>
