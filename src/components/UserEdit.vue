<template>
    <div class="component">
        <h3>Edit User</h3>
        <p>Tuoi cua toi: {{ age }} </p>
        <p>Ten toi : {{ name }}</p>
        <button>Thay doi</button>
    </div>
</template>

<script>
export default {
    name : "user-edit",
    methods : {
        onChange(){

        }
    },
    props : ['age','name']
}
</script>
