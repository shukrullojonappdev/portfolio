<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <div class="logos">
      <img alt="Vue logo" class="vue logo" src="@/assets/logo.svg" />
      <img alt="Angular logo" class="angular logo" src="@/assets/angular.svg" />
      <img alt="Nestjs logo" class="nestjs logo" src="@/assets/nestjs-icon.svg" />
    </div>
    <div class="wrapper">
      <HelloWorld msg="Salom!" />
      <nav>
        <RouterLink to="/">Asosiy</RouterLink>
        <RouterLink to="/projects">Proyektlar</RouterLink>
        <RouterLink to="/about">Aloqa</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
  text-align: center;
}

.logos {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 140px;
  width: 100%;
  margin-bottom: 20px;
}

.logo {
  width: 140px;
  height: 140px;
  margin: 0 auto 2rem;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}
.angular {
  top: -10px;
  width: 155px;
  height: 155px;
  animation: angularlogo 3s linear infinite;
}

.vue {
  opacity: 1;
  animation: vuelogo 3s linear infinite;
}

.nestjs {
  opacity: 0;
  top: 9px;
  width: 122px;
  height: 122px;
  animation: nestlogo 3s linear infinite;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1200px) {
  .logos {
    margin-right: 40px;
  }

  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}

@keyframes angularlogo {
  from {
    opacity: 0;
    transform: rotateY(0deg);
  }
  16% {
    opacity: 0;
  }
  17% {
    opacity: 1;
    transform: rotateY(90deg);
  }
  33% {
    opacity: 1;
    transform: rotateY(180deg);
  }
  49% {
    opacity: 1;
  }
  50% {
    opacity: 0;
    transform: rotateY(270deg);
  }
  66% {
    opacity: 0;
    transform: rotateY(360deg);
  }
  82% {
    opacity: 0;
  }
  83% {
    opacity: 0;
    transform: rotateY(450deg);
  }
  to {
    opacity: 0;
    transform: rotateY(540deg);
  }
}

@keyframes nestlogo {
  from {
    opacity: 0;
    transform: rotateY(0deg);
  }
  16% {
    opacity: 0;
  }
  17% {
    opacity: 0;
    transform: rotateY(90deg);
  }
  33% {
    opacity: 0;
    transform: rotateY(180deg);
  }
  49% {
    opacity: 0;
  }
  50% {
    opacity: 1;
    transform: rotateY(270deg);
  }
  66% {
    opacity: 1;
    transform: rotateY(360deg);
  }
  82% {
    opacity: 1;
  }
  83% {
    opacity: 0;
    transform: rotateY(450deg);
  }
  to {
    opacity: 0;
    transform: rotateY(540deg);
  }
}

@keyframes vuelogo {
  from {
    opacity: 1;
    transform: rotateY(0deg);
  }
  16% {
    opacity: 1;
  }
  17% {
    opacity: 0;
    transform: rotateY(90deg);
  }
  33% {
    opacity: 0;
    transform: rotateY(180deg);
  }
  49% {
    opacity: 0;
  }
  50% {
    opacity: 0;
    transform: rotateY(270deg);
  }
  66% {
    opacity: 0;
    transform: rotateY(360deg);
  }
  82% {
    opacity: 0;
  }
  83% {
    opacity: 1;
    transform: rotateY(450deg);
  }
  to {
    opacity: 1;
    transform: rotateY(540deg);
  }
}
</style>
