<script setup>

defineProps({
  event: {
    type: Object,
    required: true
  }
})

</script>

<template>
  <RouterLink :to="{name:'event-detail',params:{id: event.id}}">
    <div class="event-card">
      <h2>{{ event.title }}</h2>
      <span>@{{ event.time }} on {{ event.date }}</span>
    </div>
    </RouterLink>
</template>

<style scoped>
.event-card {
  padding: 1.5rem;
  border: 1px solid #39495c;
  width: 250px;
  margin: 0.5rem 0.5rem;
  cursor: pointer;
  font-size: small;
}

.event-card:hover {
  box-shadow: 0 15px 30px 0 rgba(0, 0, 0, 0.2);
  background-color: mediumseagreen;
}
</style>
