<template>
    <div>
        <img :src="product.image" :alt="alt">
        <h1>{{ product.name }}</h1>
        <h2 v-if="product.available">Available</h2>
        <h2 v-else>Out of Stock</h2>
        <p>Price: {{ formattedPrice }}</p>
    </div>
</template>

<script>
export default {
    name: 'ProductDetails',

    data() {
        return {
            product: {
                name: 'kitekat',
                price: '99.99',
                available: true,
                image: require('../assets/korm.jpg'),
                alt: 'korm',
            },
        }
    },

    computed: {
        formattedPrice: function () {
            return `$${this.product.price}`;
        }
    }
};
</script>

<style lang="scss" scoped>

</style>