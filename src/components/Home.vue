<template>
  <v-container fluid>
    <v-layout row wrap>
      <v-flex xs12 class="text-xs-center" mt-4>
        <h1>{{name}}</h1>
      </v-flex>
      <v-jumbotron>
        <v-container fill-height>
          <v-layout align-center>
            <v-flex class="text-xs-center">
              <h3 class="display-2">To Be Done</h3>
              <span class="subheading">Lorem ipsum dolor sit amet, pri veniam forensibus id. Vis maluisset molestiae id, ad semper lobortis cum.</span>
              <v-divider class="my-3"></v-divider>
              <v-btn v-for="(route, i) of routes" :key="i" :to="route.route" :color="route.color" class="mx-0" large outline>
                <v-icon large>{{route.icon}}</v-icon>
              </v-btn>
            </v-flex>
          </v-layout>
        </v-container>
      </v-jumbotron>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      name: 'Home'
    }
  },
  computed: {
    routes() {
      return [
        {
          route: { name: 'User' },
          name: 'User',
          icon: 'person_pin',
          color: 'primary',
          iconColor: 'primary',
        },
        {
          route: { name: 'ToDo' },
          name: 'To Do',
          icon: 'format_list_numbered',
          color: 'primary',
          iconColor: 'primary',
        },
      ]
    }
  }
}
</script>
