<script setup>
import EventCard from '@/components/EventCard.vue'
import { ref } from 'vue'

const events = ref([
    {
      id: 5928101,
      category: 'animal welfare',
      title: 'Cat Adoption Day',
      description: 'Find your new feline friend at this event',
      location: 'Meow Town',
      date: 'January 28, 2025',
      time: '12:00',
      petsAllowed: true,
      organizer: 'Kat Laydee'
    }, {
      id: 5928102,
      category: 'animal welfare',
      title: 'Cat Playing Day',
      description: 'Find your new feline player friend at this event',
      location: 'Meow Town',
      date: 'January 28, 2025',
      time: '12:00',
      petsAllowed: true,
      organizer: 'Kat Laydee'
    }, {
      id: 5928103,
      category: 'animal welfare',
      title: 'Cat Demo Day',
      description: 'Find your new feline friend at this event',
      location: 'Meow Town',
      date: 'January 28, 2025',
      time: '12:00',
      petsAllowed: true,
      organizer: 'Kat Laydee'
    }

  ]
)

</script>

<template>
  <h1>Events for good</h1>
  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event"></EventCard>
  </div>
</template>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
