<template>
  <v-container>
    <v-row>
      <v-col>
        Testing
      </v-col>
    </v-row>
    <v-row>
      <v-col
        v-for="(product, index) in productStore.products"
        :key="index"
        cols="12"
        md="4"
      >
        <StoreItem :product="product"></StoreItem>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts" setup>
  import { useProductStore } from '../stores/ProductStore';
  import { onMounted } from 'vue';
  import StoreItem from "./StoreItem.vue";
  
  const productStore = useProductStore();
  onMounted(() => {
    productStore.init();
    console.log(productStore.products);
  });
  
  
  //productStore.init();
  console.log(productStore.products);

  
</script>
