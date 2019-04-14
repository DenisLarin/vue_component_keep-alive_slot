<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <br>
                <button class="btn btn-primary" @click="selectedComponent = 'appBlue'">Load Blue Template</button>
                <button class="btn btn-success" @click="selectedComponent = 'appGreen'">Load Green Template</button>
                <button class="btn btn-danger" @click="selectedComponent = 'appRed'">Load Red Template</button>
                <hr>
                <app-blue>
                    <h1>blue component</h1>
                    <p>blue content</p>
                </app-blue>
                <app-green>
                    <h1>green component</h1>
                    <p>green content</p>
                </app-green>
                <app-red>
                    <h1>red component</h1>
                    <p>red content</p>
                </app-red>
                <hr>
                <component :is="selectedComponent">
                </component>
            </div>
        </div>
    </div>
</template>

<script>
    import Blue from './components/Blue.vue';
    import Green from './components/Green.vue';
    import Red from './components/Red.vue';

    export default {
        data(){
            return{
                selectedComponent: "appBlue",
            }
        },
        components: {
            appBlue: Blue,
            appGreen: Green,
            appRed: Red
        }
    }
</script>

<style>
</style>
