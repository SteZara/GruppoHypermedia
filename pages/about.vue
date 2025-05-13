<script setup lang="ts">
var isMobile =  /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator?.userAgent); 
</script>

<template>
    <breadcrumb />
    <div id="founders_div">
        <img src="~/public/founders/founder_icon.png" width="50px"/>
        <b style="color: var(--name-color); font-size: xx-large;"> The founders </b>
        <span style="font-weight: 200;"> The heart of Yoga Center is our passionate and experienced team of instructors and wellness professionals </span>
        <div class="founders_images">
            <figure>
                <img src="~/public/founders/stefano_zara.png"/>
                <figcaption>Stefano Zara</figcaption>
            </figure>
            <figure>
                <img src="~/public/founders/circle.png" />
                <figcaption>Founder</figcaption>
            </figure>
            <figure>
                <img src="~/public/founders/circle.png" />
                <figcaption>Founder</figcaption>
            </figure>
            <figure>
                <img src="~/public/founders/circle.png" />
                <figcaption>Founder</figcaption>
            </figure>

            <!-- <img src="~/public/founders/founder2.png" width="100px"/> -->
            <!-- <img src="~/public/founders/founder3.png" width="100px"/> -->
        </div>
    </div>
    <div id="about_section">
        At Yoga Center, we believe that yoga is more than just a practice it's a way of life. 
        Founded with the intention of creating a welcoming space for growth, healing, and connection, our center offers a peaceful retreat from the noise of everyday life. 
        Whether you're a beginner or an experienced yogi, our diverse classes, experienced instructors, and supportive community are here to guide you on your journey.
        <br><br>
        We offer a variety of yoga styles including Hatha, Vinyasa, Bikram,  Kundalini and Ashtanga, as well as meditation sessions, wellness workshops, and holistic therapies. 
        Our mission is to nurture mind-body awareness, encourage inner peace, and empower each individual to live with intention and balance.
        <br><br>
        Come as you are, and leave feeling renewed.
    </div>
    <div id="bottom_logo">
        <img src="~/public/center_icon.png" width="50px"/> 
    </div>
</template>

<style scoped>

figcaption {
    color: var(--name-color);
    text-align: center;
    font-weight: 400;
}

.founders_images {
    /* width: 50vw; */
    display: flex;
    justify-content:space-evenly;
    gap: 20px;
}
.founders_images img {
    justify-self: center;
    max-width: 100px;
    max-height: 100px;
    width: 10vmax;
    height: 10vmax;
    border-radius: 50%;
    object-fit: cover;
}
figure {
     /* display: block; */
     margin: 0; 
}

#founders_div {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 20px; 
}

#about_section {
    margin: 0 auto;
    padding-top: 20px;
    padding-bottom: 20px;

    width: 60vw; 

    text-align: center;

    font-size: 20px;
    font-weight: 400;
    line-height: 20px;
    word-wrap: break-word;
}

#bottom_logo {
    padding-top: 10px;
    padding-bottom: 10px;
    display: flex;
    justify-content: center;
}
</style>