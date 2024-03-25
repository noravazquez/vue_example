<template>
    <div>
        <div>Fullname: {{ fullName }}</div>
    </div>
</template>

<script>
import { ref, computed } from "vue";

export default {
    setup() {
        const firstName = ref("Nora");
        const lastName = ref("Vazquez");

        const fullName = computed(() => {
            return `${firstName.value} ${lastName.value}`
        })

        return {
            fullName,
        };
    },
};
</script>