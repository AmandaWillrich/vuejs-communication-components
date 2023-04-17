<template>
    <section>
        <div class="main-container">
            <header>
                <h1>Add Friends</h1>
            </header>
            <user-data @set-data="setUserData"></user-data>
            <active-user
            :name="friends.name"
            :age="friends.age"></active-user>
        </div>

    </section>
</template>

<script>

export default {
    data() {
        return {
            friends: {
                id: 'amanda',
                name: 'Amanda Willrich',
                age: 27
            }
        }
    },
    methods: {
        setUserData(name, age) {
            this.friends = {
                name: name,
                age: Number(age) // you can also convert to number with: +age
            }
        } // this method, which is being listened in the user-data,
        // gets the same parameters passed on the emit of our component method
        // the method sets the new data to the entered data
    }
}

</script>

<style>
* {
    box-sizing: border-box;
}

html {
    font-family: 'Jost', sans-serif;
}

body {
    margin: 0;

}

label {
    padding: 16px;
}

input {
    padding: 10px;
    border: 1px solid black;
    border-radius: 5px;
}

button {
    margin: 16px;
    padding: 6px 13px 6px 13px;
    background-color: rgba(132, 0, 255, 0.651);
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button:hover {
    background-color: rgb(153, 57, 243);
}

.main-container {
    text-align: center;
}

.card {
    text-align: center;
    padding: 10px 50px 10px 50px;
    margin: 32px;
    display: inline-block;
    border: 1px solid black;
    border-radius: 16px;
}

.form {
    padding: 16px;
}

.labels {
    padding: 16px;
}

</style>