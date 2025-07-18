<script setup>
import { ref } from "vue";
import Main from "./Main.vue"

const schedule = ref([
  {
    date: "23 July 2025",
    events: [
      { time: "8:00", name: "Registration & arrival of guests", venue: "LT7" },
      { time: "9:00", name: "Opening ceremony", venue: "LT7", events: [
        { time: "9:00", name: "National anthem & recitation of Du'aa", venue: "LT7", speaker: "Mr Raja Harith", institute: "Sunway University" },
        { time: "9:05", name: "Welcoming remarks", venue: "LT7", speaker: "Prof Ir Dr Denny Ng Kok Sum", institute: "Sunway University" },
        { time: "9:10", name: "Opening remarks", venue: "LT7", speaker: "Prof Dr Ali Abdalhussein Jazie", institute: "University of Al-Qadisiyah" },
        { time: "9:15", name: "Welcoming speech", venue: "LT7", speaker: "Dr Salah M Khaleel", institute: "Iraqi Cultural Attaché Advisor" },
        { time: "9:20", name: "Opening ceremony & group photo session", venue: "LT7" },
      ] },
      { time: "10:00", name: "Keynote 1", venue: "LT7", title: "Advanced Materials for Energy Storage and Heat Transfer Applications", speaker: "Prof Dr Saidur Rahman" },
      { time: "10:45", name: "Tea break", venue: "LT7" },
      { time: "11:00", name: "Keynote 2", venue: "LT7", title: "Toward 2035: Renewable Energy Innovations Transforming Our Future", speaker: "AP Dr Hj Firas Basim Alnaimi" },
      { time: "11:45", name: "Keynote 3", venue: "LT7", title: "Hydrogen Storage and Safety: Innovations, Challenges, and Industrial Applications", speaker: "AP Dr Ali Sameer Muhsan" },
      { time: "12:30", name: "Lunch", venue: "LT7" },
      { time: "14:00", name: "Physical presentation", venue: "LT7" },
      { time: "15:15", name: "Tea break", venue: "LT7" },
      { time: "15:30", name: "Physical presentation", venue: "LT7" },
      { time: "16:30", name: "End of day 1", venue: "" },
    ]
  },
  {
    date: "24 July 2025",
    events: [
      { time: "9:30", name: "Keynote 4", venue: "LT7", title: "Advanced Techonolgy Vehicles", speaker: "AP Dr Hj Firas Basim Alnaimi" },
      { time: "10:15", name: "Tea break", venue: "LT7" },
      { time: "10:45", name: "Keynote 5", venue: "LT7", title: "Rubbercrete Bricks: Pioneering Sustainable Construction with Scrap Tire Innovation", speaker: "Ir AP Dr Bashar S Mohammed" },
      { time: "11:30", name: "Keynote 6", venue: "LT7", title: "Engineering Innovation: From Control to Creativity", speaker: "Ir Dr Chua Yaw Long" },
      { time: "12:15", name: "Lunch", venue: "LT7" },
      { time: "14:00", name: "Campus tour", venue: "Sunway University" },
      { time: "15:15", name: "Tea break", venue: "LT7" },
      { time: "15:45", name: "Closing ceremony", venue: "LT7" },
      { time: "16:45", name: "End of day 2", venue: "" },
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
        <Timeline :value="day.events" pt:eventcontent:class="relative -top-1" pt:eventopposite:class="relative -top-1 !basis-20 !grow-0 !shrink-0">
          <template #opposite="slotProps">{{ slotProps.item.time }}</template>
          <template #content="slotProps">
            <!-- <div> -->
            <Fieldset v-if="slotProps.item.title" pt:root:class="relative -top-3">
              <template #legend>{{ slotProps.item.name }} ({{ slotProps.item.venue }})</template>
              <div class="flex flex-col">
                <span class="font-bold">{{ slotProps.item.title }}</span>
                <span class="text-right" v-if="slotProps.item.speaker">by {{ slotProps.item.speaker }}</span>
              </div>
            </Fieldset>
            <Fieldset v-else-if="slotProps.item.events" pt:root:class="relative -top-3">
              <template #legend>{{ slotProps.item.name }} ({{ slotProps.item.venue }})</template>
              <Timeline :value="slotProps.item.events" pt:eventcontent:class="relative -top-1" pt:eventopposite:class="relative -top-1 !basis-20 !grow-0 !shrink-0">
                <template #opposite="sp">{{ sp.item.time }}</template>
                <template #content="sp">
                  <div class="flex flex-col">
                    <span>{{ sp.item.name }}</span>
                    <span class="text-right" v-if="sp.item.speaker">by {{ sp.item.speaker }}</span>
                    <span class="text-right" v-if="sp.item.institute">{{ sp.item.institute }}</span>
                  </div>
                </template>
              </Timeline>
            </Fieldset>
            <div v-else class="ml-[30px]">{{ slotProps.item.name }} <span v-if="slotProps.item.venue">({{ slotProps.item.venue }})</span></div>
            <!-- </div> -->
          </template>
        </Timeline>
      </Panel>
    </template>
  </Card>
</template>