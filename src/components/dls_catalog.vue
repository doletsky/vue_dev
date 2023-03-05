<template>
    <div id="dls_catalog">
        <h3>Catalog</h3>
        <dls-item 
            v-for="product in products"
            :key="product.article"
            :product_data="product"
        >
        </dls-item>
    </div>
</template>

<script>
    import dlsItem from './dls_item.vue'
    export default {
        name: 'dls_catalog',
        props: {},
        data() {
            return {
                products: [
                    {
                        image: "1.jpg",
                        name: "T-shift 1",
                        price: 100,
                        article: "T1",
                        available: true
                    },
                    {
                        image: "2.jpg",
                        name: "T-shift 2",
                        price: 150,
                        article: "T2",
                        available: true
                    },
                    {
                        image: "3.jpg",
                        name: "T-shift 3",
                        price: 200,
                        article: "T3",
                        available: false
                    },
                    {
                        image: "4.jpg",
                        name: "T-shift 4",
                        price: 250,
                        article: "T4",
                        available: true
                    },
                    {
                        image: "5.jpg",
                        name: "T-shift 5",
                        price: 300,
                        article: "T5",
                        available: true
                    },
                    {
                        image: "6.jpeg",
                        name: "T-shift 6",
                        price: 350,
                        article: "T6",
                        available: true
                    }
                ]
            }
        },
        components: {
            dlsItem
        }

    }
</script>

<style lang="scss">
    #dls_catalog {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
    }
</style>