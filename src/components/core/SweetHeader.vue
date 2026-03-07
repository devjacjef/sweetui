<script setup lang="ts">
import type { SweetBase } from "@/types/shared";
import { computed } from "vue";

interface SweetHeader extends SweetBase {}

const props = withDefaults(defineProps<SweetHeader>(), {
    sweet: true,
});

const classes = computed(() => ({
    "sweet-header": props.sweet,
}));
</script>

<template>
    <header :class="classes">
        <slot></slot>
    </header>
</template>

<style>
.sweet-header {
    min-width: 100vw;
}
</style>
