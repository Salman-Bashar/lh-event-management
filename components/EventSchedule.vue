<!-- <template>
  <div class="p-8">
    <h1 class="font-bold text-2xl mb-8">Event Schedule</h1>
    <div class="grid grid-cols-3 gap-8">
      <div v-for="conference in conferences" :key="conference.id" class="flex flex-col items-start" >
        <NuxtLink :to="`/event/${conference.id}`">
          <h2 class="font-bold">{{conference.name}}</h2>
        </NuxtLink>
        <div class="text-sm text-gray-800">
          <p>Organized By: {{conference.organizer.name}}</p>
          <p>Date: {{conference.schedule.day}}</p>
          <p>Location: {{conference.schedule.location}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import gql from 'graphql-tag'

export default {
  name: 'EventSchedule',
  apollo: {
    conferences: gql`
      query ALL_CONFERENCES_QUERY {
        conferences {
          id
          name
          organizer {
            name
          }
          schedules {
            day
            location
          }
        }
      }
    `,
  },
}
</script> -->
