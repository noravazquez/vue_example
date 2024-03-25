<template>
    <div>
        <div>{{ counter }}</div>
        <div>{{ obj }}</div>
    </div>
</template>

<script>
import { reactive, ref } from "vue";

export default {
    setup() {
        const counter = ref(0);
        const obj = reactive({ counter: 0});

        setInterval(() => counter.value++, 500);
        setInterval(() => obj.counter++, 500);

        return {
            counter, obj,
        }
    },
};
</script>