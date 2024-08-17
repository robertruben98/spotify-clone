<script setup>

import HomeCard from "@/components/HomeCard.vue";
import CategorySelect from "@/components/CategorySelect.vue";
</script>

<template>
  <div class="p-8">
    <button
        type="button"
        class="text-white text-2xl font-semibold hover:underline cursor-pointer"
    >
      Podcasts to make you smarter
    </button>

    <div class="py-1.5"></div>
    <div class="grid xl:grid-cols-5 lg:grid-cols-4 md:grid-cols-3 sm:grid-cols-2 gap-6">
      <CategorySelect category="Music" image="https://picsum.photos/id/1/300/300/" />
      <CategorySelect category="Movies" image="https://picsum.photos/id/2/300/300/" />
      <CategorySelect category="Books" image="https://picsum.photos/id/3/300/300/" />
      <CategorySelect category="Fitness" image="https://picsum.photos/id/4/300/300/" />
      <CategorySelect category="Technology" image="https://picsum.photos/id/5/300/300/" />
      <CategorySelect category="Travel" image="https://picsum.photos/id/6/300/300/" />
      <CategorySelect category="Photography" image="https://picsum.photos/id/7/300/300/" />
      <CategorySelect category="Food" image="https://picsum.photos/id/8/300/300/" />
      <CategorySelect category="Education" image="https://picsum.photos/id/9/300/300/" />
      <CategorySelect category="Art" image="https://picsum.photos/id/10/300/300/" />
      <CategorySelect category="Gaming" image="https://picsum.photos/id/11/300/300/" />
      <CategorySelect category="Health" image="https://picsum.photos/id/12/300/300/" />
      <CategorySelect category="Science" image="https://picsum.photos/id/13/300/300/" />
      <CategorySelect category="Fashion" image="https://picsum.photos/id/14/300/300/" />
      <CategorySelect category="Business" image="https://picsum.photos/id/15/300/300/" />
      <CategorySelect category="History" image="https://picsum.photos/id/16/300/300/" />
      <CategorySelect category="Sports" image="https://picsum.photos/id/17/300/300/" />
      <CategorySelect category="Nature" image="https://picsum.photos/id/18/300/300/" />
      <CategorySelect category="Comedy" image="https://picsum.photos/id/19/300/300/" />
      <CategorySelect category="News" image="https://picsum.photos/id/20/300/300/" />

    </div>
  </div>
</template>
