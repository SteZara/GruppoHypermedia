<template>
    <div id="top_bar_icon">
        <img src="~/public/center_icon.png" width="40px">
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

#top_bar_icon {
    margin-left: 5px;
}

nav {
    display: flex;
    gap: 10px;
    justify-content: center;
    align-items: center;
}

nav a {
    width: 4em;
    transition: 0.2s ease-out;
}

nav>a:hover {
    color: #4f7275;
    font-weight: 900;
}

#top_bar_search {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
    margin-right: 10px;
}

</style>