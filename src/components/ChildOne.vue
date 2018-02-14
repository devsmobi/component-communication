<template>
    <div id="child-1">
        <h3 class="title">{{ title }}</h3>
        <p>{{ message }}</p>
        <input type="text" placeholder="Write something..." v-model="something">
        <button @click="submit">Submit</button>
    </div>
</template>

<script>
    export default{
        name: 'child-one',
        props: ['message'],
        data: function () {
            return {
                title: 'Child 1',
                something: ''

            }

        },
        methods: {
            submit: function () {
                if (this.something.length === 0) {
                    return
                }
                this.$emit('somethingSent', this.something)
            }
        }
    }
</script>

<style>
    #child-1 {
        height: 200px;
        background-color: green;
        border: 3px solid black;
        margin: 5px;
        padding: 5px;
    }
</style>