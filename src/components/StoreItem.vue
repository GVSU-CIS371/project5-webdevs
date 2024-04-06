<template>
  <v-card
    variant="outlined"
    hover
    :title="props.product.name"

  >
  </v-card>
</template>

<script lang="ts" setup>
import { Product } from "../types/product";

type Props = {
  product: Product;
}
const props = defineProps<Props>();


</script>
