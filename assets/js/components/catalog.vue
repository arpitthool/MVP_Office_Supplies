<template>
    <div>
        <div class="row">
            <div class="col-12">
                <h1>
                    Products
                </h1>
            </div>
        </div>
        <div class="row">
            <div class="col-xs-12 col-6 mb-2 pb-2">
                TODO - load some products!
            </div>
        </div>
        <div class="row">
            <span class="p-3">
                <legend-component :title="legend" />
            </span>
        </div>
    </div>
</template>

<script>
import axios from 'axios';
import LegendComponent from '@/components/legend.vue';

export default {
    name: 'Catalog',
    components: {
        LegendComponent,
    },
    data() {
        return {
            products: [],
            legend: "Shipping takes 10-12 weeks, and products probably won't work",
        };
    },
    async mounted() {
        const response = await axios.get('/api/products');
        this.products = response.data['hydra:member'];
    },
};
</script>
