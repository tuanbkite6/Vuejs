<template>
    <div class="component">
        <h3>User Details</h3>
        <p>Tuoi toi: {{ age }}</p>
        <p>Ten toi : {{ name }}</p>
    </div>
</template>

<script>
    export default {
        props  : ['age','name']
    }
</script>
