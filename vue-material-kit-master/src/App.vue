<template>
  <div id="material-kit">
    <div :class="{ 'nav-open': NavbarStore.showNavbar }">
      <router-view name="header" />
      <main>
        <fade-transition origin="center" mode="out-in" :duration="250">
        <router-view />
        </fade-transition>
      </main>
      <router-view name="footer" />
    </div>
  </div>
</template>
