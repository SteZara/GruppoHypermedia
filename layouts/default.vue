<script setup>
import { onMounted, ref, onBeforeMount } from 'vue';

const isScrolled = ref(false);
var header_div = null;
const handleScroll = () => {
    if (window.scrollY > 0) {
        // console.log('scrolled');
        isScrolled.value = true;
        header_div?.setAttribute('isScrolled', isScrolled.value.toString());
    } else {
        isScrolled.value = false;
        header_div?.setAttribute('isScrolled', isScrolled.value.toString());
        // isScrolled.value = false;
    }
};
onBeforeMount(() => {
  // Check if the page is already scrolled on mount
  header_div = document.querySelector('header'); 
  header_div.setAttribute('isScrolled', isScrolled.value.toString());
});
onMounted(() => {
  header_div = document.querySelector('header'); 
  // header_div?.setAttribute('isScrolled', isScrolled.value.toString());
  // isScrolled: false;

  window.addEventListener('scroll', handleScroll);
  // Cleanup the event listener when the component is unmounted
  return () => {
      window.removeEventListener('scroll', handleScroll);
  };
});

</script>

<template>
  <link href="https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@300;400;600;700&display=swap" rel="stylesheet">
  <header>
    <header_content />
  </header>
  <main>
    <!-- <breadcrumb/> -->
    <NuxtPage/>
  </main>
  <footer>
    <footer_content />
  </footer>
</template>

<style scoped>

main{
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  padding: 10px; 

  scrollbar-width: none;
}

header {
  top: 0;
  position: sticky;

  display: flex;    
  max-height: 100px;
  align-items: center;
  justify-content: space-between;

  backdrop-filter: blur(10px);
  background-color: var(--azure-transparent); 

  /* opacity: 0.8; */
  /* box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.1); */
  padding: 2px;
  text-align: center;

  transition: 0.2s;
}

header[isScrolled='true'] {
  transition: 0.2s;
  /* max-height: 20px; */
  /* background-color: var(--azure); */
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
}

footer {
  padding: 20px;
  background: linear-gradient(180deg, #3D8D8F 0%, #265559 85%);
  flex-direction: column;
}

</style>