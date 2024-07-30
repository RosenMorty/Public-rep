<template>
  <div class="itembar-user">
    <img 
      :src="image"
      alt="ItemPreview"
      class="itembar-image"
    >
    <div class="itembar-text">
      <h1 class="itembar-title">
        {{ title }}
      </h1>
      <div class="itembar-email">
        {{ email }}
      </div> 
      <div class="itembar-phone">
        {{ phone }}
      </div> 
      <div class="itembar-about">
        {{ about }}
      </div> 
    </div> 
  </div>
</template>

<script>

export default {
    props: {
        id: {
          type: Number,
          required: true
        },
        image: {
          type: String,
          required: true
        },
        title: {
          type: String,
          required: true
        },
        email: {
          type: String,
          required: true
        },
        phone: {
          type: String,
          required: true
        },
        about: {
          type: String,
          required: true
        }
    }
}

</script>

<style lang="scss" scoped>
    
</style>