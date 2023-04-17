<template>
    <div class="card">
        <h2><strong>Name:</strong> {{ name }}</h2>
        <h3><strong>Age:</strong> {{ age }} years old</h3>
    </div>
</template>

<script>
export default {
    props: {
        name: {
            type: String,
            required: true
        },
        age: {
            type: Number,
            required: true
        }
    }
}
</script>