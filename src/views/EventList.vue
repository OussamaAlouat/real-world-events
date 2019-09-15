<template>
  <div>
    <h1>Events</h1>
    <EventCard />
    <router-link :to="{ name: 'event-show', params: {id: '1' } }">Show event</router-link>
  </div>
</template>

<script>
import EventCard from '@/components/EventCard.vue';
export default {
  components: {
    EventCard
  }
}
</script>

<style>

</style>