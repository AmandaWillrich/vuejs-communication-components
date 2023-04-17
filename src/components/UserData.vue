<template>
    <div>
        <form class="form" @submit.prevent="submitData">
            <div class="labels">
                <input type="text" placeholder="Name" v-model="enteredName" />
            </div>
            <div>
                <input type="text" placeholder="Age" v-model="enteredAge" />
            </div>
            <button>Add Friend</button>
            <hr>
        </form>
    </div>
</template>

<script>
export default {
    emits: ['set-data'], // it has to know which emits are being created
    data() {
        return {
            enteredName: '',
            enteredAge: ''
        }
    },
    methods: {
        submitData() {
            this.$emit('set-data', this.enteredName, this.enteredAge) //emits a custom event
            //first argument is the name of the event, in this case set-data
        }
    }
}

</script>