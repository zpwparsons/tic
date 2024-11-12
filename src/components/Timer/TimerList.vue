<script setup lang="ts">
import PrimaryButton from '@/components/Buttons/PrimaryButton.vue'
import GhostButton from '@/components/Buttons/GhostButton.vue'
import TimerListItem from '@/components/Timer/TimerListItem.vue'
import type { Timer } from '@/types';

const { heading, timers } = defineProps({
  heading: String,
  timers: Array<Timer>,
});
</script>

<template>
  <section>
    <div class="px-1 flex items-center justify-between">
      <div class="flex items-center gap-4">
        <h3 class="text-xl font-semibold text-slate-900">{{ heading }}</h3>
        <p class="text-md text-slate-500 font-medium">June 14, 2024</p>
      </div>

      <div class="flex gap-4">
        <GhostButton>Clear All</GhostButton>
        <PrimaryButton>New Timer</PrimaryButton>
      </div>
    </div>

    <div class="my-6 bg-white shadow">
      <div class="border-t border-slate-100">
        <ul class="divide-y divide-slate-100">
          <TimerListItem v-for="timer in timers" :key="timer.id" :timer="timer" />
        </ul>
      </div>
    </div>

    <div class="px-1 flex justify-end">
      <div class="flex items-center gap-4 text-sm text-slate-800 uppercase">
        Total <p class="text-lg font-semibold text-slate-900">05:00</p>
      </div>
    </div>
  </section>
</template>
