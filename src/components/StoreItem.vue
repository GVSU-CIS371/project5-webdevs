<template>
  <v-card
    variant="outlined"
    hover
    :title="product.name"
    :subtitle="ratingStr"
    :text="product.description"
    :prepend-avatar="product.image"
  >
  </v-card>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import { ProductDoc } from "../types/product";
type Props = {
  product: ProductDoc;
}
const props = defineProps<Props>();
const product = props.product.data;
const ratingStr = ref(product.rating + "/5")
//console.log(product);


</script>
