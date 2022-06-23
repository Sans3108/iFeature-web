<script setup>
import top_bar from './components/top_bar.vue';
import bottom_bar from './components/bottom_bar.vue';

const getDeviceType = () => {
  const ua = navigator.userAgent;
  if (/(tablet|ipad|playbook|silk)|(android(?!.*mobi))/i.test(ua)) {
    return "tablet";
  }
  if (
    /Mobile|iP(hone|od)|Android|BlackBerry|IEMobile|Kindle|Silk-Accelerated|(hpw|web)OS|Opera M(obi|ini)/.test(
      ua
    )
  ) {
    return "mobile";
  }
  return "desktop";
};

if (['mobile', 'tablet'].includes(getDeviceType())) {
  alert("This site is not optimized for your device! We're working on that...");
}
</script>

<template>
  <div class="wrapper">
    <top_bar />
    <div class="content">
      <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Voluptas a, eligendi consequatur cum, assumenda saepe
        vitae laborum quam aspernatur atque adipisci repellat unde nemo ex odio quo doloribus delectus dignissimos amet
        cumque maiores iusto architecto? Magnam odit ullam mollitia eveniet blanditiis! Ducimus repellat similique
        architecto ipsum quasi dolore, commodi suscipit eaque quidem, eveniet, beatae enim praesentium rem ut! Aliquam
        voluptatem laboriosam maxime quisquam similique ducimus, aliquid omnis sequi at, quibusdam cupiditate cumque
        porro voluptate quam voluptas, sed sint adipisci odio ratione repudiandae suscipit eos veritatis recusandae?
        Totam tenetur voluptatem, architecto natus libero doloribus praesentium ea laudantium ullam assumenda vitae
        maxime nulla molestiae perferendis sed possimus nisi aperiam temporibus inventore et nam repellat porro mollitia
        dolorum! Consequuntur quaerat officiis mollitia placeat eum atque earum hic omnis quos ad. Doloremque, ex maxime
        facere autem ipsam tempora error expedita dignissimos, aliquam delectus modi. Aspernatur natus exercitationem
        vitae ipsa in ad error hic. Aperiam inventore, eveniet animi molestias libero unde odio adipisci! Alias mollitia
        debitis ipsum necessitatibus unde nam, cumque eaque at beatae ullam illum repellendus. Velit alias aspernatur
        distinctio reprehenderit quis autem iste, quam laboriosam eaque, deserunt nemo blanditiis repellendus ratione a
        eveniet ea ipsa maxime officiis laudantium tempora eius quas dolore. Quo.</p>
    </div>
    <bottom_bar class="social" />
  </div>
</template>

<style>
@import './variables.css';
@import url("https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

/* semantic color variables for this project */
:root {
  --background-color: #181818;
  --background-color-soft: #222222;
  --background-color-mute: #282828;

  --border-color: rgba(84, 84, 84, 0.48);
  --border-color-hover: rgba(84, 84, 84, 0.65);

  --heading-color: #ffffff;
  --text-color: rgba(235, 235, 235, 0.85);
}

/*
@import url('https://fonts.googleapis.com/css2?family=Amatic+SC:wght@400;700&display=swap');

font-family: 'Amatic SC', cursive;
*/

*,
*::before,
*::after {
  box-sizing: border-box;
  position: relative;
  font-weight: normal;
  font-family: Nunito, Inter, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell,
    "Fira Sans", "Droid Sans", "Helvetica Neue", sans-serif;
  margin: 0;
  padding: 0;
}

body {
  min-height: 100vh;
  color: var(--text-color);
  background: var(--background-color);
  font-size: 15px;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.wrapper {
  display: flex;
  flex-direction: column;
  height: 100vh;
  width: 100%;
}

.social {
  position: absolute;
  bottom: 0;
}

p {
  font-size: 1.2rem;
  line-height: 1.5;
  display: flex;
  justify-self: center;
  margin: 3%;
}
</style>
