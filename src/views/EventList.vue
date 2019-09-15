<template>
  <div>
    <h1>Events</h1>
    <EventCard v-for="event in events" :key="event.id"/>
  </div>
</template>

<script>
import EventCard from '@/components/EventCard.vue';
import axios from 'axios';

export default {
  components: {
    EventCard
  },
  data() {
    return {
      events: []
    }
  },
  created() {
    axios.get('http://localhost:3000/events')
      .then(response => {
        console.log(response.data);
        this.events = response.data;
      })
      .catch(err => {
        console.log(err);
      });
  }
}
</script>

<style>

</style>