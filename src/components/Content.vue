<template>
  <div class="content">
    <p class="content-page">
      <font-awesome-icon :icon="['fas', 'chevron-left']" size="xs" />
      Minha conta
    </p>

    <h1 class="content-title">Bolsas Favoritas</h1>
    <p class="content-description">Adicione bolsas de cursos e faculdade do seu interesse e receba atualizações com as melhores ofertas disponíveis.</p>
    
    <div>
      <div>Todos os semestres</div>
      <div>1° semestre de 2021</div>
      <div>2° semestre de 2021</div>
    </div>

    <button>
      <font-awesome-icon class="plus-icon" :icon="['fas', 'plus']" size="5x" />
      <h4>Adicionar bolsa</h4>
      <p>Clique para adicionar bolsas de cursos do seu interesse</p>
    </button>
  </div>  
</template>

<style lang="scss">
.content{
  width: 100%;
  height: 100vh;
  background-color: $gray-background;

  padding: 20px;

  &-page{
    font-weight: 600;
    color: $secondary-blue;

    font-size: 1.2rem;
    margin: 0 0 15px 0;
  }

  &-title{
    margin: 0 0 10px 0;
  }

  &-description{
    font-size: 1.3rem;
  }

  .plus-icon{
    border: 5px solid $secondary-blue;
    border-radius: 100%;
    padding: 10px;
    color: $secondary-blue;
  }
}
</style>