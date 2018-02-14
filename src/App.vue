<template>
    <div class="container">
        <div id="parent">
            <div class="row">
                <div class="col-md-12">
                    <h2 class="title">{{ msg }}</h2>
                    <br>
                    <br>
                    <h4>Message from Child 1:{{ something }}</h4>
                </div>
                <!--<div class="row">-->
                <div class="col-md-6">
                    <!--<child-one message="Message to child 1" @somethingSent="updateSomething($event)"></child-one>-->
                    <child-one message="Message to child 1" @somethingSent="something = $event"></child-one>
                </div>
                <div class="col-md-6">
                    <child-two :second-message=messageTwo third-message="Message to Child 3"></child-two>
                    <input type="text" v-model="messageTwo">
                </div>
            </div>
        </div>
        <!--<div class="row">-->
        <!--<div class="col-md-12">-->
        <!--<h2 class="title">Child 4</h2>-->
        <!--</div>-->
        <!--</div>-->
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
                something: '',
                messageTwo: 'Message to child 2'
            }
        },
        methods: {
            updateSomething: function ($event) {
                this.something = $event
            }
        }
    }
</script>

<style>
    .container {
        margin-top: 40px;
    }

    #parent {
        height: 550px;
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
