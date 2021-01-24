<template>
    <div class="container-fluid">
        <div class="row">
            <aside class="col-xs-12 col-3">
                <sidebar />
            </aside>
            <div class="col-xs-12 col-9">
                <catalog />
            </div>
        </div>
    </div>
</template>

<script>
import Catalog from '../components/catalog';
import Sidebar from '../components/sidebar';

export default {
    name: 'Products', //for debugging purpose alwats give a name.
    components: {
        Catalog,
        Sidebar,
    },
};
</script>
