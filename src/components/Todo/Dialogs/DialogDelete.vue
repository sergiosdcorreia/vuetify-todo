<template>
  <v-dialog v-model="dialog" persistent max-width="290">
    <v-card>
      <v-card-title class="headline">
        Delete task?
      </v-card-title>
      <v-card-text>Are you sure you wanna delete this task?</v-card-text>
      <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn text @click="$emmit('close')">
          No
        </v-btn>
        <v-btn color="red" text @click="$store.dispatch('deleteTask', task.id)">
          Yes
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  props: ['task'],
  data: () => ({
    dialog: false,
  }),
};
</script>

<style></style>
