<template>
  <router-link
    class="event-link"
    :to="{ name: 'EventDetails', params: { id: event.id } }"
  >
    <div class="event-card">
      <span>@ {{ event.time }} on {{ event.date }}</span>
      <h4>{{ event.title }}</h4>
    </div>
  </router-link>
</template>

<script>
export default {
  name: "EventCard",
  props: {
    event: Object,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.event-card {
  display: flex;
  text-align: center;
  justify-content: center;
  flex-direction: column;
  border: 2px solid #2c3e50;
  padding: 40px;
  margin-block: 10px;
  color: #2c3e50;
}

.event-link {
  text-decoration: none;
}
</style>
