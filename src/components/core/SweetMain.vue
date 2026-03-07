<script setup lang="ts">
import type { SweetBase } from "@/types/shared";
import { computed } from "vue";

interface SweetMain extends SweetBase {}

const props = withDefaults(defineProps<SweetMain>(), {
    sweet: true,
});

const classes = computed(() => ({
    "sweet-main": props.sweet,
}));
</script>

<template>
    <main :class="classes">
        <slot></slot>
    </main>
</template>

<style>
.sweet-main {
    height: 100vh;
}
</style>
