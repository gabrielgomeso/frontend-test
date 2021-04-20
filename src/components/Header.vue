<template>
  <header class="header">
    <div class="header-block">
      <i class="fa fa-question-circle"></i>
      <font-awesome-icon :icon="['fas', 'question-circle']" size="2x" />
      Ajuda
    </div>
    <div class="header-block">
      <p class="header-block--logo">
      </p>
    </div>
    <div class="header-block">
      <font-awesome-icon :icon="['fas', 'user-circle']" size="2x" />
      Conta
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
// USAR BEM SEMPRE
.header {
  // positioning
  display: grid;
  grid-template-columns: auto 1fr auto;
  

  // colors
  color: $secondary-blue;

  // font formating
  font-size: 1.5rem;
  font-weight: 600;

  &-block {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    
    padding: 10px;
    grid-gap: 5px;

    &--logo {
      display: flex;
      flex-direction: column;
      align-items: center;
      width: 100%;
      height: 100%;
      border-right: 3px solid $lightgray-border;
      border-left: 3px solid $lightgray-border;
    }
  }
}
</style>
