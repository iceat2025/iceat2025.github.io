<script setup>
import { ref } from "vue";
import Main from "./Main.vue"

const schedule = ref([
  {
    date: "23 July 2025",
    events: [
      { time: "10:00", name: "Opening", venue: "LT7" },
      { time: "10:00", name: "Opening", venue: "LT7" },
      { time: "10:00", name: "Opening", venue: "LT7" },
    ]
  },
  {
    date: "24 July 2025",
    events: [
      { time: "10:00", name: "Opening", venue: "LT7" },
      { time: "10:00", name: "Opening", venue: "LT7" },
      { time: "10:00", name: "Opening", venue: "LT7" },
    ]
  }
])
</script>

<template>
  <Main></Main>
  <Card pt:content:class="text-center flex flex-col gap-3">
    <template #title><span class="font-light">Schedule</span></template>
    <template #content>
      <Panel v-for="day in schedule" pt:header:class="!justify-center font-bold">
        <template #header>{{ day.date }}</template>
        <Timeline :value="day.events">
          <template #opposite="slotProps">{{ slotProps.item.time }}</template>
          <template #content="slotProps">{{ slotProps.item.name }}({{ slotProps.item.venue }})</template>
        </Timeline>
      </Panel>
    </template>
  </Card>
</template>