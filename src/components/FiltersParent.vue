<template>
    <div>
        <Filters @change="onChange"/> <!-- Si limita a propagare l'evento al genitore -->
    </div>
</template>
<script>
import Filters from './Filters.vue';

export default {
    name: 'FiltersParent',
    data: () => {
        return {
            value: 'none',
        };
    },
    components: {
        Filters,
    },
    props: {
    },
    methods: {
        onChange(selectedValue) {
            this.$emit('change', selectedValue);
        }
    }
}
</script>
