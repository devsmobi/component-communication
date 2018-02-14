<template>
    <div class="container">
        <div id="parent">
            <div class="row">
                <div class="col-md-12">
                    <h2 class="title">{{ msg }}</h2>
                </div>
                <!--<div class="row">-->
                <div class="col-md-6">
                    <child-one message="Message to child 1"></child-one>
                </div>
                <div class="col-md-6">
                    <child-two :second-message=messageTwo third-message="Message to Child 3"></child-two>
                    <input type="text" v-model="messageTwo">
                </div>
            </div>
        </div>
        <div class="row">
            <p>Another Child</p>
        </div>
    </div>
</template>

<script>
    import ChildOne from './components/ChildOne.vue'
    import ChildTwo from './components/ChildTwo.vue'

    export default {
        name: 'app',
        components: {
            childOne: ChildOne,
            ChildTwo
        },
        data () {
            return {
                msg: 'Parent',
                messageTwo: 'Message to child 2'
            }
        }
    }
</script>

<style>
    .container {
        margin-top: 40px;
    }

    #parent {
        height: 430px;
        background-color: red;
        border: 3px solid black;
        margin-bottom: 2px;
    }

    .title {
        color: white;
        text-align: center;
        padding-top: 50px;
    }
</style>
