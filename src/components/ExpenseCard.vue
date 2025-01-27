<template>
    <v-card class="pa-4" max-width="400" outlined>
      <v-card-title>{{ title }}</v-card-title>
      <v-card-subtitle>{{ subtitle }}</v-card-subtitle>
      <v-card-text>
        <p>{{ description }}</p>
      </v-card-text>
      <v-card-actions>
        <v-btn color="primary" @click="onEdit">Editar</v-btn>
        <v-btn color="error" @click="onDelete">Excluir</v-btn>
      </v-card-actions>
    </v-card>
  </template>
  
  <script lang="ts">
  export default {
    name: 'ExpenseCard',
    props: {
      title: String,
      subtitle: String,
      description: String
    },
    methods: {
      onEdit() {
        this.$emit('edit');
      },
      onDelete() {
        this.$emit('delete');
      }
    }
  };
  </script>
  
  <style scoped>
  .v-card {
    margin: 10px 0;
  }
  </style>
  