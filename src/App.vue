<script setup lang="ts">
import TimerList from '@/components/Timer/TimerList.vue'

const timers = [
  {
    id: '4cda642b-e233-49c4-aa73-4db309927da8',
    label: 'FSP-100',
    time: '05:00',
  },
  {
    id: '6568e881-0e74-435c-a22b-7c8c8e5ded6e',
    label: 'FSP-110',
    time: '02:33',
  },
];
</script>

<template>
  <main class="p-12 min-h-full h-screen">
    <div class="flex flex-col gap-8">
      <TimerList heading="Today" :timers="timers" />
    </div>
  </main>
</template>
