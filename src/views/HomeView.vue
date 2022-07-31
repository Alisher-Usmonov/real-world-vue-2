<template>
  <div class="home">
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from "@/components/EventCard.vue";

export default {
  name: "HomeView",
  components: {
    EventCard,
  },
  data() {
    return {
      events: [
        {
          id: 6930113,
          category: "dev community",
          title: "GDG Tashkent 2022",
          description: "Google I/O and Google Developers Group",
          location: "INHA University",
          date: "January 28, 2022",
          time: "10:00",
          organizer: "GDG Tashkent",
        },
        {
          id: 5438284,
          category: "dev community",
          title: "#GoNight 2022",
          description: "Google I/O and Google Developers Group",
          location: "INHA University",
          date: "August 20, 2022",
          time: "17:00",
          organizer: "GoNight Tashkent",
        },
        {
          id: 22131278,
          category: "dev community",
          title: "#GoNight 2022",
          description: "Google I/O and Google Developers Group",
          location: "INHA University",
          date: "August 20, 2022",
          time: "17:00",
          organizer: "GoNight Tashkent",
        },
      ],
    };
  },
};
</script>
