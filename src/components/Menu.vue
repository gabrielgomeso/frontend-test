<template>
  <nav class="navigation">
    <a href="" class="navigation-link">Minha Conta</a>
    <a href="" class="navigation-link">Menu ˅</a>

  </nav>
</template>


<style lang="scss">
  .navigation{
    width: 100%;
    height: 40px;
    background: $primary-blue;

    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 10px 0 10px;
    box-shadow: inset 1px 1px 3px 1px rgba(128, 128, 128, 0.418);

    &-link{
      font-weight: 600;
      text-decoration: none;
      color: #FFFFFF;
      font-size: 1.5rem;
    }
  }
</style>