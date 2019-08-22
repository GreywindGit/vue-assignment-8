<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <br>
                <button class="btn btn-primary" @click="selectedComponent = 'appBlue'">Load Blue Template</button>
                <button class="btn btn-success" @click="selectedComponent = 'appGreen'">Load Green Template</button>
                <button class="btn btn-danger" @click="selectedComponent = 'appRed'">Load Red Template</button>
                <hr>
                <component :is="selectedComponent">
                    <h3 slot="title">{{ title }}</h3>
                    <p slot="artist">by {{ artist }}</p>
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
        data: function() {
            return {
                selectedComponent: 'appBlue',
                componentDetails: {
                    appBlue: {
                        title: 'Blue Suede Shoes',
                        artist: 'Elvis Presley'
                    },
                    appGreen: {
                        title: 'O Green World',
                        artist: 'Gorillaz'
                    },
                    appRed: {
                        title: 'Wrapped in Red',
                        artist: 'Kelly Clarkson'
                    }
                }
            }
        },
        computed: {
                title: function() { return this.componentDetails[this.selectedComponent].title },
                artist: function() { return this.componentDetails[this.selectedComponent].artist }
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
