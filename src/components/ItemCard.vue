<template>
  <div :class="['cardbar-user',isActive && 'cardbar-user__active']">
    <img 
      :src="`${selected.image}`"
      :alt="selected.title"
      class="cardbar-image"
    >
    <div class="cardbar-text">
      <h1 class="cardbar-title">
        {{ selected.title }}
      </h1>
      <div class="cardbar-email">
        {{ selected.email }}
      </div> 
    </div> 
  </div>
</template>

<script setup>

defineProps({
  selected: {
    type: Object,
    required: true,
    default: () => {}
  },
  isActive: {
    type: Boolean,
    default: false
  }
});

</script>

<style lang="scss">

.cardbar {
  &-text {
    margin: 15px 0 18px 15px;
  }
  &-user__active {
    border: 2px solid grey;
    background-color: #E0E0E0;
  }
  &-user:hover {
    background-color: #E0E0E0;
  }
  &-user {
    width: 240px;
    height: 70px;
    border-radius: 10px;
    overflow: hidden;
    background: #FFF;
    box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.10);
    display: flex;
    box-sizing:border-box;
    margin-bottom: 18px;
  }
  &-image {
    width: 70px; 
    height: 70px;
    border-right: 1px solid #E0E0E0;
  }
  &-title {
    width: 100%;
    height: 15px;
    color: #333;
    font-family: Montserrat;
    font-size: 14px;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
    margin-bottom: 5px;
  }
  &-email {
    color: #76787D;
    font-family: Montserrat;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
  }
}
</style>