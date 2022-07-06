<template>
  <div>
    <section>
      <div class="user-container">
        <div>
          <i class="fas fa-child fa-2x"></i>
        </div>
        <div class="user-description">
            {{ modal.user }}
          <div class="time">{{ modal.time_ago }}</div>
        </div>
      </div>
      <h2>{{ modal.title }}</h2>
    </section>
    <section>
      <div v-html="modal.content"></div>
    </section>
  </div>
</template>
<script>
export default {
  name: 'ModalAsk',
  components: {},
  props: [
      'modal',
  ],
  data() {
    return {
      item: {}
    }
  },
}
</script>

<style scoped>
.user-container {
  display: flex;
  align-items: center;
  padding: 0.5rem;
}
.user-description {
  padding-left: 8px;
}
.time {
  font-size: 0.7rem;
}
</style>