<template>
    <div class="event-details">
      <div class="details">
        <span class="category">{{ event.category }}</span>
        <span class="organizer">{{ event.organizer }}</span>
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  import { defineProps } from 'vue'
  import type { Event } from '@/type'
  
  defineProps<{
    event: Event
  }>()
  </script>
  
  <style scoped>
  .event-details {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    
  }
  
  .details {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    
  }
  
  .category, .organizer {
    padding: 20px;
    width: 250px;
  cursor: pointer;
  border: 1px solid #39495c;
  margin-bottom: 19px;    
  }
  </style>