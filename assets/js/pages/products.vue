<template>
    <h1>Hello {{ firstName }}! is this cooler?</h1>
</template>

<script>
export default {
    name: 'Products', //for debugging purpose
    data() {
        return {
            firstName: 'Arpit',
        };
    },
};
</script>
