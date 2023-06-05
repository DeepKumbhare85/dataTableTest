<template>
  <p>This is for testing purpose</p>
  <VTextField v-model="search" placeholder="Search ..." variant="outlined" class="w-50"></VTextField>

  <VDataTable v-model:items-per-page="itemsPerPage" v-model:page="currentPage" :headers="headers" :items="desserts"
    :search="search" item-value="name">
  </VDataTable>
</template>

<script lang="ts" setup>
//data table
import { ref } from 'vue';
const itemsPerPage = ref(5)
const currentPage = ref(1)
const search = ref('')
// const sortBy= [{ key: 'calories', order:'desc'}]

const headers = [
  {
    title: 'Dessert (100g serving)',
    key: 'name',
  },
  { title: 'Calories', key: 'calories' },
  { title: 'Fat (g)', key: 'fat' },
  { title: 'Carbs (g)', key: 'carbs' },
  { title: 'Protein (g)', key: 'protein' },
  { title: 'Iron (%)', key: 'iron' },
];

const desserts = [
  {
    name: 'Frozen Yogurt',
    calories: 159,
    fat: 6.0,
    carbs: 24,
    protein: 4.0,
    iron: '1',
  },
  {
    name: 'Jelly bean',
    calories: 375,
    fat: 0.0,
    carbs: 94,
    protein: 0.0,
    iron: '0',
  },
  {
    name: 'KitKat',
    calories: 518,
    fat: 26.0,
    carbs: 65,
    protein: 7,
    iron: '6',
  },
  {
    name: 'Eclair',
    calories: 262,
    fat: 16.0,
    carbs: 23,
    protein: 6.0,
    iron: '7',
  },
  {
    name: 'Gingerbread',
    calories: 356,
    fat: 16.0,
    carbs: 49,
    protein: 3.9,
    iron: '16',
  },
  {
    name: 'Salmon',
    calories: 206,
    fat: 13.2,
    carbs: 0,
    protein: 22,
    iron: '1%'
  },
  {
    name: 'Spinach',
    calories: 23,
    fat: 0.4,
    carbs: 3.6,
    protein: 2.9,
    iron: '15%'
  },
  {
    name: 'Peanut Butter',
    calories: 190,
    fat: 16,
    carbs: 7,
    protein: 7,
    iron: '4%'
  },
  {
    name: 'Quinoa',
    calories: 120,
    fat: 2,
    carbs: 21,
    protein: 4,
    iron: '15%'
  },
  {
    name: 'Greek Yogurt',
    calories: 130,
    fat: 0,
    carbs: 9,
    protein: 23,
    iron: '0%'
  },
  {
    name: 'Sweet Potato',
    calories: 86,
    fat: 0.1,
    carbs: 20,
    protein: 1.6,
    iron: '4%'
  },
  {
    name: 'Almonds',
    calories: 161,
    fat: 14,
    carbs: 6,
    protein: 6,
    iron: '8%'
  },
  {
    name: 'Egg',
    calories: 78,
    fat: 5,
    carbs: 0.6,
    protein: 6,
    iron: '5%'
  },
  {
    name: 'Avocado',
    calories: 234,
    fat: 21,
    carbs: 12,
    protein: 2.9,
    iron: '4%'
  },
  {
    name: 'Brown Rice',
    calories: 216,
    fat: 2,
    carbs: 45,
    protein: 5,
    iron: '8%'
  },
  {
    name: 'Ice cream sandwich',
    calories: 237,
    fat: 9.0,
    carbs: 37,
    protein: 4.3,
    iron: '1',
  },
  {
    name: 'Lollipop',
    calories: 392,
    fat: 0.2,
    carbs: 98,
    protein: 0,
    iron: '2',
  },
  {
    name: 'Cupcake',
    calories: 305,
    fat: 3.7,
    carbs: 67,
    protein: 4.3,
    iron: '8',
  },
  {
    name: 'Honeycomb',
    calories: 408,
    fat: 3.2,
    carbs: 87,
    protein: 6.5,
    iron: '45',
  },
  {
    name: 'Donut',
    calories: 452,
    fat: 25.0,
    carbs: 51,
    protein: 4.9,
    iron: '22',
  },
  {
    name: 'Chicken Breast',
    calories: 165,
    fat: 3.6,
    carbs: 0,
    protein: 31,
    iron: '2%'
  },
  {
    name: 'Banana',
    calories: 105,
    fat: 0.4,
    carbs: 27,
    protein: 1.3,
    iron: '1%'
  },
  {
    name: 'Cheeseburger',
    calories: 303,
    fat: 12,
    carbs: 33,
    protein: 16,
    iron: '16%'
  },
  {
    name: 'Hummus',
    calories: 166,
    fat: 9,
    carbs: 14,
    protein: 8,
    iron: '10%'
  },
  {
    name: 'Salmon',
    calories: 206,
    fat: 13,
    carbs: 0,
    protein: 22,
    iron: '1%'
  },
  {
    name: 'Peanut Butter',
    calories: 94,
    fat: 8,
    carbs: 3,
    protein: 4,
    iron: '3%'
  },
  {
    name: 'Oatmeal',
    calories: 147,
    fat: 2.5,
    carbs: 27,
    protein: 5,
    iron: '20%'
  },
  {
    name: 'Spinach',
    calories: 23,
    fat: 0.4,
    carbs: 3.6,
    protein: 2.9,
    iron: '21%'
  },
  {
    name: 'Beef Stew',
    calories: 235,
    fat: 7.5,
    carbs: 18,
    protein: 23,
    iron: '23%'
  },
  {
    name: 'Rice',
    calories: 130,
    fat: 0.3,
    carbs: 28,
    protein: 2.7,
    iron: '1%'
  },
  {
    name: 'Pizza',
    calories: 285,
    fat: 10,
    carbs: 35,
    protein: 13,
    iron: '15%'
  },
  {
    name: 'Grapes',
    calories: 62,
    fat: 0.3,
    carbs: 16,
    protein: 0.6,
    iron: '1%'
  },
  {
    name: 'Avocado',
    calories: 234,
    fat: 21,
    carbs: 12,
    protein: 3,
    iron: '4%'
  },
  {
    name: 'Carrots',
    calories: 41,
    fat: 0.2,
    carbs: 10,
    protein: 1,
    iron: '2%'
  },
  {
    name: 'Pork Chop',
    calories: 221,
    fat: 12,
    carbs: 0,
    protein: 25,
    iron: '3%'
  },
  {
    name: 'Brownie',
    calories: 371,
    fat: 20,
    carbs: 48,
    protein: 3,
    iron: '15%'
  },
  {
    name: 'Mushrooms',
    calories: 22,
    fat: 0.3,
    carbs: 3.3,
    protein: 2.2,
    iron: '3%'
  },
  {
    name: 'Egg',
    calories: 78,
    fat: 5,
    carbs: 0.6,
    protein: 6,
    iron: '5%'
  },
];

</script>
