<script setup>
defineProps({
  item: Object,
  deleteFromCart: Function,
});
</script>

<template>
  <article
    class="flex justify-between items-center gap-3 border border-slate-200 p-3 rounded-xl transition hover:shadow-md rounded-lg"
  >
    <img class="w-16 h-16 md:w-24 md:h-24" :src="item.imageUrl" alt="Sneakers" />
    <div>
      <h2 class="text-sm md:text-xl">{{ item.title }}</h2>
      <b class="md:text-xl">{{ item.price }} ₴</b>
    </div>
    <img
      class="h-8 self-end cursor-pointer transition opacity-40 hover:opacity-100 rounded-lg"
      src="/close.svg"
      alt="Delete"
      @click="() => deleteFromCart(item.id)"
    />
  </article>
</template>
