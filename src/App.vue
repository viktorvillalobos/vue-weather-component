<template>
    <div id="app">
        <vue-weather-component :enable-credits="true"></vue-weather-component>
    </div>
</template>

<script>
    import VueWeatherComponent from '@/components/vue-weather-component'

    export default {
        name: 'App',

        components: {
            VueWeatherComponent
        },

        data() {
            return {
                currentDay: {
                    icon: 'fog',
                    temp: '17',
                    currentSummary: 'Fog.',
                    hourlySummary: 'Partly cloudy throughout the day.',
                    windSpeed: 6
                }
            }
        }
    }
</script>

<style>

</style>
