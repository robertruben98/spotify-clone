<script setup>
import {ref, toRefs, watchEffect} from "vue";
import {useRoute} from "vue-router";
const route = useRoute();

const props = defineProps({
  iconString: String,
  iconSize: Number,
  pageUrl: String,
  name: String
});
const {iconString, pageUrl, name, iconSize} = toRefs(props);

let icon = ref(null);
let textIsHover = ref(false);

watchEffect(() => {
  const isActive = route.path === pageUrl.value;
  icon.value = iconString.value + (isActive ? '-active' : '-inactive');
  textIsHover.value = isActive;
})

const isHover = () => {
  if (icon.value === iconString.value + '-active') return;
  const isInactive = icon.value === iconString.value + '-inactive';
  icon.value = iconString.value + (isInactive? '-inactive-hover' : '-inactive');
  textIsHover.value = isInactive;
}

</script>

<template>
  <li
      class="flex items-center justify-start pb-4 cursor-pointer"
      @mouseover="isHover"
      @mouseleave="isHover"
  >
   <img :width="iconSize" :src="`/images/icons/${icon}.png`">
    <div
        :class="textIsHover ? 'text-white' : 'text-gray-400'"
        class="font-semibold text-[14px] ml-4 mt-0.5"
    >
      <span :class="route.path === pageUrl ? 'text-white' : ''">
        {{name}}
      </span>
    </div>
  </li>
</template>
