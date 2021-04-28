<template>
  <div class="contacts">
    <div class="contacts-contact">
      <font-awesome-icon :icon="['fab', 'whatsapp']" size="3x" />
      <div class="contacts-contact--text">
        <span class="contacts-contact--phone-number">0800 123 2222</span>
        <span class="contacts-contact--worktime">
          Segunda a sexta de 8h às 22h
        </span>
      </div>
    </div>
    <div class="contacts-contact">
      <font-awesome-icon :icon="['fas', 'comments']" size="3x" />
      <p>Chat</p>
    </div>
    <div class="contacts-contact">
      <font-awesome-icon :icon="['fas', 'envelope']" size="3x" />
      <p>E-mail</p>

    </div>
    <div class="contacts-contact">
      <font-awesome-icon :icon="['fas', 'info-circle']" size="3x" />
      <p>Ajuda</p>

    </div>
  </div>
  
</template>
<style lang="scss">
  .contacts{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 2px;
    background: #50D3E8;
    color: white;
    

    &-contact:first-child{
      grid-area: 1 / 1 / span 1 / span 3;
      display: grid; 
      grid-template-columns: auto auto;
    }

    &-contact{
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      
      gap: 10px;
      font-size: 1.2rem;
      font-weight: 600;
      padding: 20px;
      background: #007A8D;

      &--text{
        display: flex;
        flex-direction: column;
        gap: 5px;
      }

      &--worktime{
        font-weight: 400;
      }
      
    }
  }
</style>