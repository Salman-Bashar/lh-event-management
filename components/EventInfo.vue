<template>
  <div class="p-8">
    <h1 class="font-bold text-2xl mb-8">Event Information</h1>
    <div>
      <p>Event Name: {{conference.name}}</p>
      <p>Year: {{conference.year}}</p>
      <p>Starting Date: {{conference.startDate}}</p>
    </div>
  </div>
</template>

<script>
import gql from 'graphql-tag'

const CONFERENCE = gql`
  query getConference($id: ID!) {
    conference(id: $id) {
      id
      name
      year
      startDate
    }
  }
`;

export default {
  name: 'EventInfo',
  apollo: {
    query: CONFERENCE,
  }
}
</script>