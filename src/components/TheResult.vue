<template>
  <div class="resultbar-search">
    <span
      v-if="!userStore.selectedUser"
      class="resultbar-text"
    >
      Выберите сотрудника, чтобы посмотреть его профиль
    </span>
    <div
      v-else
      class="resultbar-image"
    >
      <div>
        <img
          :src="userStore.selectedUser.image"
          class="resultbar-image__cart"
        >
      </div>
      <div class="resultbar-info"> 
        <div class="resultbar-title">
          {{ userStore.selectedUser.title }}
        </div>
        <div class="resultbar-email">
          email: <span class="resultbar-email__text">
            {{ userStore.selectedUser.email }}
          </span>
        </div>
        <div class="resultbar-phone">
          phone: <span class="resultbar-phone__text">
            {{ userStore.selectedUser.phone }}
          </span>
        </div>
        <div class="resultbar-about">
          О себе:
        </div>
        <div class="resultbar-about__text">
          {{ userStore.selectedUser.about }}
        </div>
      </div> 
    </div>
  </div>
</template>


<script setup>
import { useSelectedUserStore } from '../store/SelectedUser'

const userStore = useSelectedUserStore()

</script>


<style scoped lang="scss">
    .resultbar {
        &-search {
            display: flex;
        }
        &-info {
            margin: 30px 236px 0 0;
        }
        &-text {
            color: #76787D;
            font-family: "Inter", sans-serif;
            font-size: 14px;
            font-style: normal;
            font-weight: 400;
            line-height: normal;
            display: flex;
            margin: 250px 550px;
        }
        &-image {
            display: flex;
        }
        &-image__cart { 
            width: 424px;
            height: 286px;
            margin: 30px 61px 0 21px;
            border: 1px solid #E0E0E0;
            background:  lightgray 50% / cover no-repeat, #FFF;
            display: flex;
            border-radius: 10px;
        }
        &-title {
            width: 100%;
            height: 19px;
            color: #000;
            font-family: "Montserrat", sans-serif;
            font-size: 16px;
            font-style: normal;
            font-weight: 600;
            line-height: 140%; 
            margin-bottom: 10px;
        }
        &-email {
            width: 100%;
            height: 21px;
            color: #333;
            font-family: "Inter", sans-serif;
            font-size: 14px;
            font-style: normal;
            font-weight: 600;
            line-height: 140%;
            margin-bottom: 10px;
        }
        &-email__text {
            color: #76787D;
            font-family: "Inter", sans-serif;
            font-size: 14px;
            font-style: normal;
            font-weight: 400;
            line-height: 140%;
        }
        &-phone {
            width: 100%;
            height: 21px;
            color: #333;
            font-family: "Inter", sans-serif;
            font-size: 14px;
            font-style: normal;
            font-weight: 600;
            line-height: 140%;
            margin-bottom: 20px;
        }
        &-phone__text {
            color: #76787D;
            font-family: "Inter", sans-serif;
            font-size: 14px;
            font-style: normal;
            font-weight: 400;
            line-height: 140%;
        }
        &-about {
            width: 233px;
            color: #333;
            font-family: "Inter", sans-serif;
            font-size: 16px;
            font-style: normal;
            font-weight: 600;
            line-height: 140%;
            display: flex;
            flex-direction: column;
            margin-bottom: 25px;
        }
        &-about__text {
            width: 439px;
            color: #76787D;
            font-family: "Inter", sans-serif;
            font-size: 14px;
            font-style: normal;
            font-weight: 400;
            line-height: normal;
        }
    }
</style>