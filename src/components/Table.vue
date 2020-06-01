<template>
  <v-simple-table>
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">API</th>
          <th class="text-left">Status</th>
          <th class="text-left">Documentation</th>
          <th class="text-left">Gitlab</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="item in routes" :key="item.name">
          <td>{{ item.name }}</td>
          <td>
            <v-img
              alt="Status img"
              class="shrink mr-2"
              contain
              src="@/assets/green.png"
              transition="scale-transition"
              max-width="15"
              max-height="15"
            />
            {{ item.status }}
          </td>
          <td>
            <a href="https://www.w3schools.com">{{ item.documentation }}</a>
          </td>
          <td>
            <a href="https://www.w3schools.com">{{ item.gitlab }}</a>
          </td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
</template>

<script>
export default {
  data() {
    return {
      routes: [
        {
          name: "Start Interaction",
          status: "Available",
          documentation: "Link",
          gitlab: "Link",
        },
        {
          name: "Get Interactions",
          status: "Available",
          documentation: "Link",
          gitlab: "Link",
        },
        {
          name: "Get Party",
          status: "Available",
          documentation: "Link",
          gitlab: "Link",
        },
        {
          name: "Identify a Party",
          status: "Available",
          documentation: "Link",
          gitlab: "Link",
        },
        {
          name: "Get Events",
          status: "Available",
          documentation: "Link",
          gitlab: "Link",
        },
        {
          name: "Post Events",
          status: "Available",
          documentation: "Link",
          gitlab: "Link",
        },
      ],
    };
  },
};
</script>
