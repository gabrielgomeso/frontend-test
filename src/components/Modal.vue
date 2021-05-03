<script>

import Database from "../../db.json";

export default {
  name: "Modal",
  data () {
    return {
      schools: Database,
    };
  },
  methods: {
    close() {
      this.$emit("close");
    },
  },
};
</script>
<template>
  <transition name="modal-fade">
    <div class="modal-backdrop">
      <button
        type="button"
        class="btn-close"
        @click="close"
        aria-label="Close modal"
      >
        <font-awesome-icon :icon="['fas', 'times']" size="2x" />
      </button>
      <div
        class="modal"
        role="dialog"
        aria-labelledby="modalTitle"
        aria-describedby="modalDescription"
      >
        <header class="modal-header" id="modalTitle">
          <slot name="header">
            <h2 class="modal-header--title">Adicionar bolsa</h2>
            <p class="modal-header--description">
              Filtre e adicione as bolsas de seu interesse.
            </p>
          </slot>
        </header>

        <section class="modal-body">
          <slot name="body" id="modalDescription">
            <label class="modal-label" for="cidade">SELECIONE SUA CIDADE</label>
            <select class="modal-select" name="cidade" id="cidade">
              <font-awesome-icon :icon="['fas', 'times']" size="2x" />

              <option value="sjc">São José</option>
              <option value="carag">Caraguá</option>
              <option value="sp">São Paulo</option>
            </select>

            <label class="modal-label" for="curso">SELECIONE SEU CURSO</label>
            <select class="modal-select" name="curso" id="curso">
              <option value="cs">Ciencia da Computacao</option>
              <option value="med">Medicina</option>
              <option value="sp">São Paulo</option>
            </select>
            <p class="modal-label">COMO VOCÊ QUER ESTUDAR?</p>
            <label for="presencial">Presencial</label>
            <input type="checkbox" id="presencial" name="presencial" checked />
            <label for="adistancia">A distância</label>
            <input type="checkbox" id="adistancia" name="adistancia" checked />

            <p class="modal-label">ATÉ QUANTO PODE PAGAR?</p>
            <input
              type="range"
              min="1"
              max="100"
              value="100"
              class="slider"
              id="myRange"
            />
          </slot>

          <!-- <li v-for="school in schools">
            {{ school.course.name }}
          </li> -->
        </section>

        <footer class="modal-footer">
          <slot name="footer">
            <button
              type="button"
              class="btn"
              @click="close"
              aria-label="Cancel"
            >
              Cancelar
            </button>

            <button
              type="button"
              class="btn-disabled"
              aria-label="Add scholarship"
              disabled
            >
              Adicionar bolsa(s)
            </button>
          </slot>
        </footer>
      </div>
    </div>
  </transition>
</template>
<style lang="scss">
select {
  -webkit-appearance: none;
  -moz-appearance: none;
  text-indent: 1px;
  text-overflow: "";
}

.modal-backdrop {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(31, 45, 48, 88%);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal {
  padding: 20px;
  min-width: 100%;
  height: auto;
  background: #ffffff;
  box-shadow: 2px 2px 20px 1px;
  
  overflow-y: auto;
  display: flex;
  flex-direction: column;
}

.modal-header {
  position: relative;

  &--title {
    font-size: 2rem;
    margin-bottom: 5px;
  }

  &--description {
    font-size: 1.5rem;
    margin-bottom: 1.5em;
  }
}

.modal-footer {
  padding-top: 10px;
  display: flex;
  gap: 10px;
  justify-content: center;
  align-items: center;
}

.modal-body {
  display: flex;
  flex-direction: column;
  gap: 15px;
  position: relative;

  .modal-label {
    font-size: 1.1rem;
    font-weight: 800;
    letter-spacing: 0.5px;
  }

  .modal-select {
    border-radius: 5px;
    padding: 10px;
    border: 1px solid #d6d9d9;
  }
}

.btn-close {
  position: absolute;
  top: 0;
  right: 0;
  border: none;
  padding: 5px;
  cursor: pointer;
  color: white;
  background: transparent;
}

.btn {
  color: $secondary-blue;
  background: #fff;
  border: 1px solid $secondary-blue;
  border-radius: 2px;
  font-weight: 600;
  padding: 15px 15px 15px 15px;
  border-radius: 5px;
  cursor: pointer;
}

.btn-disabled {
  color: #82898b;
  background: #cacdce;
  border: 1px solid #82898b;
  border-radius: 2px;
  font-weight: 600;
  padding: 15px 15px 15px 15px;
  border-radius: 5px;
}

.modal-fade-enter,
.modal-fade-leave-to {
  opacity: 0;
}

.modal-fade-enter-active,
.modal-fade-leave-active {
  transition: opacity 0.5s ease;
}
</style>

