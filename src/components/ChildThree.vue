<template>
    <div id="child-3">
        <h3 class="title">{{ title }}</h3>
        <p>{{ message }}</p>
    </div>
</template>
<script>
    export default{
        name: 'child-three',
        props:['message'],
        data: function () {
            return {
                title: 'Child 3'
            }
        }
    }
</script>
<style>
    #child-3 {
        height: 120px;
        width: 250px;
        background-color: pink;
        border: 3px solid black;
        margin: 5px;
    }
</style>