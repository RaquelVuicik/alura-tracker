<template>
    <div
        class="modal"
        :class="{ 'is-active': mostrar }"
        v-if="mostrar"
    >
        <div class="modal-background"></div>
        <div class="modal-card">
            <slot></slot>
        </div>
    </div>
</template>

<script lang="ts">

import { defineComponent } from 'vue';

export default defineComponent({
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Modal',
    props: {
        mostrar: {
            type: Boolean,
            required: true
        }
    }
})

</script>