<template>
    <div>
    <nav class="navbar">
      <div class="navbar-brand">
        <a class="navbar-item" href="/">
          My Website
        </a>
        <button
          class="navbar-burger burger"
          :class="{ 'is-active': isActive }"
          @click="toggleNavbar"
          aria-label="menu"
          aria-expanded="false"
        > X
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </button>
      </div>
  
      <div class="navbar-menu" :class="{ 'is-active': isActive }">
        <div class="navbar-start">
          <a class="navbar-item" href="/">Home</a>
          <a class="navbar-item" href="/about">About</a>
          <a class="navbar-item" href="/services">Services</a>
          <a class="navbar-item" href="/contact">Contact</a>
        </div>
      </div>
    </nav>
</div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isActive: false
      };
    },
    methods: {
      toggleNavbar() {
        this.isActive = !this.isActive;
      }
    }
  };
  </script>
  
  <style scoped>
  .navbar {
    background-color: #000000;
    padding: 10px;
    font-size: medium;
    border-radius: 10px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  
  .navbar-brand {
    display: flex;
    align-items: center;
  }
  
  .navbar-burger {
    border: none;
    background-color: transparent;
    padding: 10px;
    margin-left: auto;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  
  .navbar-burger span {
    display: block;
    width: 25px;
    height: 3px;
    background-color: #333;
  }
  
  .navbar-menu {
    display: none;
  }
  
  .navbar-menu.is-active {
    display: block;
  }
  
  .navbar-start {
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .navbar-item {
    margin-right: 10px;
    text-decoration: none;
    font-size:large;
    color: #ffe600;
    text-indent: 80px;
  }
  .navbar-item:hover{
    text-decoration: underline yellow;
  }
  
  @media screen and (max-width: 768px) {
    .navbar-menu {
      display: block;
    }
  
    .navbar-start {
      flex-direction: column;
    }
  
    .navbar-item {
      margin-right: 0;
      margin-bottom: 5px;
    }
  }
  </style>
  