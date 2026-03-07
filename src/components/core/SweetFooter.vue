<script setup lang="ts">
import type { SweetBase } from "@/types/shared";
import { computed } from "vue";

interface SweetFooter extends SweetBase {}

const props = withDefaults(defineProps<SweetFooter>(), {
    sweet: true,
});

const classes = computed(() => ({
    "sweet-footer": props.sweet,
}));
</script>

<template>
    <footer :class="classes">
        <slot></slot>
    </footer>
</template>

<style>
.sweet-footer {
    min-width: 100vw;
    position: relative;
    bottom: 0;
    left: 0;
}
</style>
