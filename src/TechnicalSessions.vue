<script setup>
import { ref } from "vue";
import Main from "./Main.vue"
import Qrcode from "vue-qrcode"

const sessions = ref([
  {
    name: "Session A: Artificial Intelligence",
    date: "23 July 2025",
    time: "10:00 - 12:30",
    qrdata: "Hi!",
    papers: [
      { id: "A1", title: "Deep Learning for Image Classification", time: "10:00 - 10:15" },
      { id: "A2", title: "Reinforcement Learning in Robotics", time: "10:15 - 10:30" },
      { id: "B1", title: "Big Data Analysis Techniques", time: "14:00 - 14:15" },
      { id: "B2", title: "Predictive Modeling with Python", time: "14:15 - 14:30" },
      { id: "B1", title: "Big Data Analysis Techniques", time: "14:00 - 14:15" },
      { id: "B2", title: "Predictive Modeling with Python", time: "14:15 - 14:30" },
      { id: "B1", title: "Big Data Analysis Techniques", time: "14:00 - 14:15" },
      { id: "B2", title: "Predictive Modeling with Python", time: "14:15 - 14:30" },
    ]
  },
  {
    name: "Session B: Data Science",
    date: "24 July 2025",
    time: "14:00 - 17:00",
    qrdata: "Ho",
    papers: [
      { id: "B1", title: "Big Data Analysis Techniques", time: "14:00 - 14:15" },
      { id: "B2", title: "Predictive Modeling with Python", time: "14:15 - 14:30" }
    ]
  }
])
</script>

<template>
  <Main></Main>
  <Card pt:content:class="text-center flex flex-col gap-3">
    <template #title><span class="font-light">Technical Sessions</span></template>
    <template #content>
      <Accordion value="0">
        <AccordionPanel v-for="(session, index) in sessions" :key="index" :value="index">
          <AccordionHeader>{{ session.name }}</AccordionHeader>
          <AccordionContent pt:content:class="flex flex-col md:flex-row items-center justify-center md:items-start md:justify-center">
            <div class="flex flex-col justify-center items-center shrink-0"><Qrcode :value="session.qrdata" scale="100" errorCorrectionLevel="L" class="w-full max-w-50"></Qrcode></div>
            <div class="flex flex-col gap-3 w-full">
              <div v-for="paper in session.papers" :key="paper.id">
                <Card>
                  <template #title>Paper ID: {{ paper.id }}</template>
                  <template #content>{{ paper.title }}</template>
                </Card>
              </div>
            </div>
          </AccordionContent>
        </AccordionPanel>
      </Accordion>
    </template>
  </Card>
</template>