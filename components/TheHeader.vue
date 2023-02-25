<template>
  <header class="header">
    <div class="container">
      <img class="logo" src="@/assets/images/logo.svg" alt="Beauty Salon" />

      <button class="header__toggle">
        <img src="@/assets/images/menu.svg" alt="" />
      </button>
    </div>
  </header>
</template>

<script>
export default {
  name: 'TheHeader',
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/helpers.scss';
.header {
  height: 4.5rem;
  border-bottom: 1px solid var(--gray-400);

  & > .container {
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  &__toggle {
    background-color: transparent;
    border: 0;
    font-size: 0;
    width: 2.25rem;
    height: 2.25rem;
  }
}

.logo {
  width: 9rem;

  @include large {
    width: 10rem;
  }
}
</style>
