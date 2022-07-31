<template>
  <div v-if="event" class="event">
    <h1>{{ event.title }}</h1>
    <p>{{ event.time }} on {{ event.date }} at {{ event.location }}</p>
    <p>{{ event.description }}</p>
  </div>
</template>

<script>
import EventService from "@/services/EventService";

export default {
  name: "EventDetailsView",
  props: ["id"],
  data() {
    return { event: null };
  },
  created() {
    EventService.getEvent(this.id)
      .then(({ data }) => {
        this.event = data;
      })
      .catch((error) => {
        console.log(error);
      });
  },
};
</script>

<style scoped>
.event {
  text-align: center;
}
</style>
