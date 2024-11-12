<script setup lang="ts">
import GhostButton from '@/components/Buttons/GhostButton.vue'
import StartIcon from '@/components/icons/StartIcon.vue'
import StopIcon from '@/components/icons/StopIcon.vue'
import type { Timer } from '@/types';
import XMarkIcon from '@/components/icons/XMarkIcon.vue'

const { timer } = defineProps<{
  timer: Timer;
}>();
</script>

<template>
  <li class="p-4 flex items-center justify-between gap-4">
    <p class="ml-2 font-semibold text-slate-900">{{ timer.label }}</p>

    <div class="flex items-center gap-1">
      <p class="mr-4 p-1 text-slate-700">{{ timer.time }}</p>

      <GhostButton>
        <StartIcon />
      </GhostButton>

      <GhostButton>
        <StopIcon />
      </GhostButton>

      <GhostButton>
        <XMarkIcon />
      </GhostButton>
    </div>
  </li>
</template>
