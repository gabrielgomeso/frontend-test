<template>
  <div class="content">
    <p class="content-page">
      <font-awesome-icon :icon="['fas', 'chevron-left']" size="xs" />
      Minha conta
    </p>

    <h1 class="content-title">Bolsas Favoritas</h1>
    <p class="content-description">
      Adicione bolsas de cursos e faculdade do seu interesse e receba
      atualizações com as melhores ofertas disponíveis.
    </p>

    <div class="content-filter">
      <div class="content-filter--option">Todos os semestres</div>
      <div class="content-filter--option">1° semestre de 2021</div>
      <div class="content-filter--option">2° semestre de 2021</div>
    </div>

    <button class="btn add-course" @click="showModal">
      <font-awesome-icon
        class="plus-icon"
        :icon="['fas', 'plus-circle']"
        size="5x"
      />
      <h4>Adicionar bolsa</h4>
      <p>Clique para adicionar bolsas de cursos do seu interesse</p>
    </button>

    <Modal v-show="isModalVisible" @close="closeModal" />
  </div>
</template>
<script>

import Modal from "./Modal.vue";


export default {
  name: "Content",
  components: {
    Modal,
  },
  data() {
    return {
      isModalVisible: false,
    };
  },
  methods: {
    showModal() {
      this.isModalVisible = true;
    },
    closeModal() {
      this.isModalVisible = false;
    },
  },
};
</script>


<style lang="scss">
.content {
  width: 100%;
  background-color: $gray-background;

  padding: 20px;

  &-page {
    font-weight: 600;
    color: $secondary-blue;

    font-size: 1.2rem;
    margin: 0 0 15px 0;
  }

  &-title {
    margin: 0 0 10px 0;
  }

  &-description {
    margin: 0 0 20px 0;

    font-size: 1.3rem;
  }

  &-filter {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    font-weight: 600;
    color: $secondary-blue;
    font-size: 1.2rem;

    margin: 0 0 20px 0;

    &--option:first-child {
      border-radius: 5px 5px 0 0;
      background: $secondary-blue;
      color: $gray-background;
    }

    &--option:last-child {
      border-radius: 0 0 5px 5px;
    }

    &--option {
      cursor: pointer;
      padding: 10px;
      border: 1px solid $secondary-blue;
      border-top: 0;
    }
  }

  .add-course {
    border: 0;
    background: $gray-background;
    box-shadow: 1px 1px 4px 1px rgb(112, 112, 112);
    padding: 25px;
    margin: 0 0 20px 0;
  }

  .plus-icon {
    margin: 0 0 10px 0;

    padding: 10px;
    color: $secondary-blue;
  }
}
</style>