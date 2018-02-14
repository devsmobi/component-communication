<template>
    <div id="child-2">
        <h3 class="title">{{ title }}</h3>
        <p>{{ secondMessage }}</p>
        <div>
            <child-three :message=message></child-three>
        </div>
    </div>
</template>

<script>
    import ChildThree from './ChildThree.vue'

    export default{
        name: 'child-two',
        props: ['second-message', 'third-message'],
        components: {
            childThree: ChildThree
        },
        data: function () {
            return {
                'title': 'Child 2',
                'message': this.thirdMessage
            }

        },
        created: function () {
            console.log(this.thirdMessage)
            console.log(this.message)
        }
    }
</script>

<style>
    #child-2 {
        height: 280px;
        background-color: lightblue;
        border: 3px solid black;
        margin: 5px;
    }

</style>