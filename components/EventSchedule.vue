<template>
  <div class="p-8">
    <h1 class="font-bold text-2xl mb-8">Event Schedule</h1>
    <div class="grid grid-cols-3 gap-8">
      <div v-for="conference in conferences" :key="conference.id" class="flex flex-col items-start" >
        <NuxtLink :to="`/event/${conference.id}`">
          <p class="font-bold">{{conference.name}}</p>
        </NuxtLink>
        <div class="text-sm text-gray-800">
          <p>Starting Date: {{conference.startDate}}</p>
        </div>
        <div class="flex-grow min-h-full">
          <nuxt-child :key="$route.params.id"></nuxt-child>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import gql from 'graphql-tag'

const ALL_CONFERENCES = gql`
  query getConferences {
    conferences {
      id
      name
      startDate
    }
  }
`

export default {
  name: "EventSchedule",
  apollo: {
    conferences: ALL_CONFERENCES,
  },
}
</script>

