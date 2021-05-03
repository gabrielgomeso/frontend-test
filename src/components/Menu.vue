<template>
  <nav class="navigation">
    <div class="navigation-links">
      <a href="" class="navigation-link">Minha Conta</a>

      <a href="" class="navigation-link">
        Menu 
        <font-awesome-icon :icon="['fas', 'chevron-down']" size="xs"/>
      </a>
    </div>

    <div class="desktop-navigation-links">
      <a href="" class="navigation-link">Minha Conta</a>
      <a href="" class="navigation-link">Pré-matrículas</a>
      <a href="" class="navigation-link">Bolsas favoritas</a>
    </div>
  </nav>
</template>


<style lang="scss">
.desktop-navigation-links {
  display: none;
}

.navigation {
  width: 100%;

  background: $primary-blue;
  box-shadow: inset 1px 1px 3px 1px rgba(128, 128, 128, 0.418);

  &-links {
    display: flex;
    align-items: center;
    justify-content: space-between;
    
  }
}

.navigation-link {
  font-weight: 600;
  text-decoration: none;
  color: #ffffff;
  font-size: 1.5rem;
  padding: 10px;
}

@media (min-width: 800px) {
  .navigation-links {
    display: none;
  }

  .desktop-navigation-links {
    display: flex;
    width: 1280px;
    margin: auto;
    justify-content: flex-start;
    .navigation-link{
      padding: 10px 25px 10px 25px;
    }
    .navigation-link:last-child{
      background: $secondary-blue;
    }
  }
}
</style>