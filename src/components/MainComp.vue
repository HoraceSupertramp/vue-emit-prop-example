<template>
    <div>
        <ul>
            <li v-for="(product, index) in filteredProducts" :key="index">{{ product.name }}</li>
        </ul>
    </div>
</template>

<script>
export default {
  name: 'MainComp',
  data() {
    return {
        products: [
            {
                name: 'Scarpa nike',
                type: 'shoes'
            },
            {
                name: 'Vestito nero',
                type: 'shirts'
            },
            {
                name: 'Jeans blue',
                type: 'pants'
            },
            {
                name: 'Pantaloncino',
                type: 'pants'
            }
        ]
    };
  },
  computed: {
    filteredProducts() {
        return this.products.filter((product) => product.type === this.selectedValue);
    }
  },
  props: {
    title: String,
    selectedValue: String,
  }
}
</script>

<style scoped lang="scss"></style>
