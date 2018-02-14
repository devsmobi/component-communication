<template>
    <div id="child-1">
        <h3 class="title">{{ title }}</h3>
        <p>{{ message }}</p>
    </div>
</template>

<script>
    export default{
        name: 'child-one',
        props:['message'],
        data: function () {
            return {
                'title': 'Child 1'
            }

        }
    }
</script>

<style>
    #child-1{
        height: 150px;
        background-color: green;
        border: 3px solid black;
        margin: 5px;
    }
</style>