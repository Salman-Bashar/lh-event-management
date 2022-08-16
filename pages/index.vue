<template>
  <div>
    <NavBar />
    <!-- <EventSchedule /> -->
  </div>
</template>

<script>
import gql from 'graphql-tag'

const ALL_CONFERENCES = gql`
  query getConferences {
    conferences {
      id
      name
      year
      startDate
    }
  }
`

export default {
  name: "IndexPage",
  apollo: {
    conferences: ALL_CONFERENCES,
  },
}
</script>
