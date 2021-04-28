<template>
  <div class="footer">
    <p class="footer-text">
      Feito com
      <font-awesome-icon
        :icon="['fas', 'heart']"
        size="sm"
        class="footer-text--icon"
      />
      pela Quero Educação
    </p>
  </div>
</template>

<style lang="scss">
.footer {
  width: 100%;
  height: 8rem;
  background-color: #18ACC4;

  display: flex;
  align-items: center;
  justify-content: center;

  &-text {
    font-size: 1.4rem;
    font-weight: 600;
    color: #ffffff;

    &--icon {
      margin: 0 5px 0 5px;
    }
  }
}
</style>