<template>
  <div class="home">
    <h1>Events For Good</h1>
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import EventService from "../services/EventService";
import EventCard from "@/components/EventCard.vue";

export default {
  name: "HomeView",
  components: {
    EventCard,
  },
  data() {
    return {
      events: null,
    };
  },
  created() {
    EventService.getEvents()
      .then(({ data }) => {
        this.events = data;
      })
      .catch((error) => {
        console.log(error);
      });
  },
};
</script>
<style scoped>
.home {
  text-align: center;
}
</style>
