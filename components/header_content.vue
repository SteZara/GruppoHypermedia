<!-- <script>
import logo from "../public/center_logo.png"; 

</script> -->

<template>
    <div id="top_bar_icon">
        <img src="~/public/center_icon.png" width="50px">
    </div>
    <div id="top_bar_nav">
        <nav>
            <NuxtLink to="/">Home</NuxtLink>
            <NuxtLink to="/activities">Activities</NuxtLink>
            <NuxtLink to="/teachers">Teachers</NuxtLink>
            <NuxtLink to="/about">About us</NuxtLink>
        </nav>
    </div>
    <div id="top_bar_search">
        <p> search </p>
        <img src="~/public/search.svg" name="search" size="24" />
    </div>
</template>

<style scoped>

nav {
    display: flex;
    gap: 20px;
    justify-content: center;
    align-items: center;
}

#top_bar_search {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
}

</style>