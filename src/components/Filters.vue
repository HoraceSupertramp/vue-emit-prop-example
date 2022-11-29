<template>
    <div>
        <select v-model="value" @change="$emit('change', value)">
            <option value="none"></option>
            <option value="shoes">shoes</option>
            <option value="shirts">shirts</option>
            <option value="pants">pants</option>
        </select>
    </div>
</template>
<script>

export default {
    name: 'Filters',
    data() {
        return {
            value: 'none',
        };
    },
}
</script>
