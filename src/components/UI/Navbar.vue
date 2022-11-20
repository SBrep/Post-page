<template>
    <div class="navbar">
        <div class="logo" @click="$router.push('/')">Vue 3</div>
        <div class="navbar__btns">
            <button @click="$router.push('/posts')">Posts</button>
            <button @click="$router.push('/about')">About</button>
            <button @click="$router.push('/store')">store</button>
            <button @click="$router.push('/composition')">composition</button>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style>
.navbar {
    height: 100px;
    background-color: black;
    color: white;
    display: flex;
    text-align: center;
    justify-content: space-around;
    align-items: center;
    font-size: large;
}
.navbar .logo {
    cursor: pointer;
}
.navbar__btns button{
    color: white;
    font-size: large;
    background: none;
    margin: 10px;
}

.navbar__btns button:hover {
    border-bottom: 2px solid white;
}

</style>