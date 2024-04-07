<template>
  <v-card
    variant="outlined"
    hover
    :title="product.name"

  >
  </v-card>
</template>

<script lang="ts" setup>
import { ProductDoc } from "../types/product";

type Props = {
  product: ProductDoc;
}
const props = defineProps<Props>();
const product = props.product.data;
console.log(product);


</script>
