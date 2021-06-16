<template>
    <div class="" style="margin-left: 30vw; margin-right: 20vw">
        <label>A simple page to allow user enter message and auto convert the message to lowercase</label>
        <b-form class="justify-content-center">
            <b-form-group
                label="Original message"
                label-cols-sm="3"
                content-cols-sm="3"
                label-align="left"
            >
                <b-form-input v-model.number="inputText" trim @update="onConvert(inputText)"></b-form-input>
            </b-form-group>
            <b-form-group
                label="Message in Lowercase"
                label-cols-sm="3"
                content-cols-sm="3"
                label-align="left"
            >
                <b-form-input v-model.number="outputText" trim></b-form-input>
            </b-form-group>
        </b-form>
    </div>
</template>

<script>
export default {
    name: 'Home',
    data () {
        return {
            inputText: '',
            outputText: '',
        }
    },
    methods:{
        onConvert(inputText){
            this.outputText = inputText.toLowerCase();
        }
    },
    mounted(){
        this.get_data()
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
