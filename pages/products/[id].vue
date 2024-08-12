<template>
  <div>
    <head>
      <Title>Nuxt App | {{ product.title }}</Title>
      <Meta name="description" :content="product.description" />
    </head>
    <ProductDetails :product="product" />
  </div>
</template>

<script setup>
const { id } = useRoute().params;
const url = "https://fakestoreapi.com/products/" + id;

//fetch the product
const { data: product } = await useFetch(url, { key: id });

// If you throw an error created with createError:
// on server-side, it will trigger a full-screen error page which you can clear with clearError.
// on client-side, it will throw a non-fatal error for you to handle. If you need to trigger a full-screen error page, then you can do this by setting fatal: true.

if (!product.value) {
  throw createError({
    statusCode: 404,
    statusMessage: "Product not found",
    fatal: true,
  });
}

definePageMeta({
  layout: "products",
});
</script>

<style scoped></style>
