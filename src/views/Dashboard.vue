<template>
    <v-container>
      <v-row>
        <v-col cols="12" md="6">
          <chart-component />
        </v-col>
        <v-col cols="12" md="6">
          <expense-card
            v-for="(expense, index) in expenses"
            :key="index"
            :title="expense.title"
            :subtitle="expense.subtitle"
            :description="expense.description"
          />
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script lang="ts">
  import ChartComponent from '@/components/ChartComponent.vue';
  import ExpenseCard from '@/components/ExpenseCard.vue';
  
  export default {
    components: {
      ChartComponent,
      ExpenseCard
    },
    data() {
      return {
        expenses: [
          { title: 'Alimentação', subtitle: 'R$ 300,00', description: 'Supermercado e Restaurantes' },
          { title: 'Transporte', subtitle: 'R$ 150,00', description: 'Ônibus e Combustível' }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  .v-row {
    margin-top: 20px;
  }
  </style>
  