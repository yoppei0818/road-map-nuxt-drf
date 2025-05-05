<script setup lang="ts"></script>

<template>
  <header>
    <a class="logo" href="#">
      <Icon name="uil:map" class="logo-icon" />
    </a>
    <nav>
      <div class="infos">
        <div class="infos-account">
          <div class="infos-account-img">
            <img src="assets/IMG_1205.jpg" alt="ユーザ名" />
          </div>
          <p class="infos-account-name">User Name</p>
        </div>
        <button class="infos-logout">
          <Icon name="uil:signout" class="infos-logout-icon" />Logout
        </button>
      </div>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem 3rem;
  width: 100%;
  height: calc(40px + 2rem);
  /* box-shadow: 0 1px 4px rgba(0, 0, 0, 0.3); */
  border-bottom: 1px solid rgba(0, 0, 0, 0.2);

  .logo {
    text-decoration: none;
    color: #000;
    display: block;
    width: 40px;
    height: 40px;
    &-icon {
      width: 100%;
      height: 100%;
    }
  }

  .infos {
    display: flex;
    align-items: center;
    justify-content: space-around;
    &-account {
      display: flex;
      align-items: center;
      margin-right: 3rem;
      &-img {
        width: 40px;
        height: 40px;
        img {
          width: 100%;
          height: auto;
        }
      }
      &-name {
        margin-left: 1rem;
      }
    }
    &-logout {
      padding: 8px 15px;
      border: none;
      border-radius: 5px;
      outline: none;
      background-color: rgba(0, 0, 0, 0.8);
      color: #fff;
      cursor: pointer;
      display: flex;
      align-items: center;
      transition: background-color 0.1s ease-in-out;
      &:hover {
        background-color: rgba(0, 0, 0, 0.6);
      }
      &-icon {
        width: 17px;
        height: 17px;
        margin-right: 5px;
      }
    }
  }
}
</style>
