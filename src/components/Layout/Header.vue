<template>
  <header class="header">
    <div class="header-top">
      <div class="header-top-search">
        <img src="/svg/header-search.svg" width="16" height="16" alt="Search icon">
      </div>
      <router-link to="/" class="header-logo">Avion</router-link>
      <div class="header-top-right">
        <div class="header-top-right__cart">
          <router-link to="/cart" >
            <img src="/svg/header-cart.svg" width="16" height="16" alt="Cart icon">
          </router-link>
        </div>

        <div class="header-top-right__user">
          <router-link to="/user">
            <img src="/svg/header-user.svg" width="16" height="16" alt="User icon">
          </router-link>
        </div>
      </div>
    </div>
    <div class="header-bottom">
      <nav class="main-nav">
        <ul class="main-nav__list">
          <li
            v-for="(item, index) of menu"
            :key="index"
            class="main-nav-item"
          >
            <router-link
              :to="item.path"
              class="main-nav__link">
              {{ item.name }}
            </router-link>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script setup>
import {ref} from 'vue';

const menu = [
  { name: 'Plant pots', path: '/plant'},
  { name: 'Ceramics', path: '/ceramics'},
  { name: 'Tables', path: '/tables'},
  { name: 'Chairs', path: '/chairs'},
  { name: 'Crockery', path: '/crockery'},
  { name: 'Tableware', path: '/tableware'},
  { name: 'Cutlery', path: '/cutlery'}
];

</script>

<style lang="scss" scoped>
.header {
  height: 132px;
  background-color: #fff;

  &-top {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 70px;
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
  }

  &-logo {
    font-family: var(--clash);
    font-size: 24px;
    font-weight: 400;
    line-height: 1.2;
    text-decoration: none;
    color: #22202E;
    &:hover {
      text-decoration: underline;
    }
  }

  &-top-right {
    display: flex;
    align-items: center;
    gap: 16px;
  }

  &-bottom {
    display: flex;
    align-items: center;
    justify-content: center;
  }
}

.main-nav {
  padding-top: 20px;
  padding-bottom: 20px;
  padding-left: 28px;
  padding-right: 28px;
}

.main-nav__list {
  display: flex;
  gap: 44px;
  margin: 0;
  padding: 0;
  list-style: none;

  @media screen and (max-width: 1024px) {
    gap: 20px;
  }
}

.main-nav__link {
  font-family: inherit;
  font-size: 16px;
  line-height: 1.2;
  text-decoration: none;
  color: #726E8D;
}
</style>