<!-- <template>
  <div class="p-8">
    <h1 class="font-bold text-2xl mb-8">Event Information</h1>
    <div>
      
    </div>
  </div>
</template>

<script>
import { gql } from 'graphql-tag'

export default {
  name: 'EventInfo',
  apollo: {
    conference: {
      query:  gql`
        query SINGLE_CONFERENCE_QUERY ($id: ID!) {
          conference(id: $id) {
            id
            name
            organizer {
              name
            }
            year
            speakers {
              name
              company
            }
          }
        }
      `,
      variables() {
        return {
          id: this.$route.params.id || 1,
        }
      }
    }
  }
}
</script> -->