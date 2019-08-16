# Vue Weather Component
Vue weather component based on darksky widgets and api.

![Preview](https://raw.githubusercontent.com/ShinZ6/vue-weather-component/master/public/preview.png)

## Project setup
```
npm install
```

## Usage

### VueJS single file component

```js
<template>
    <weather title="Weather" units="ca" :currentDay="currentDay" :forecast="forecast">
    </weather>
</template>

<script>
import VueWeatherComponent from 'vue-weather-component';

export default {
    components: {
        'weather': VueWeatherComponent
    },

    data() {
        return {
            currentDay: {
                icon: 'fog',
                temp: '17',
                currentSummary: 'Fog.',
                hourlySummary: 'Partly cloudy throughout the day.',
                windSpeed: 6
            },

            forecast: [{
                name: 'Today',
                icon: 'clear-day',
                highTemp: '37',
                lowTemp: '32'
            }, {
                name: 'Wed',
                icon: 'fog',
                highTemp: '34',
                lowTemp: '29'
            }, {
                name: 'Thu',
                icon: 'cloudy',
                highTemp: '35',
                lowTemp: '30'
            }, {
                name: 'Fri',
                icon: 'rain',
                highTemp: '32',
                lowTemp: '24'
            }, {
                name: 'Sat',
                icon: 'snow',
                highTemp: '-7',
                lowTemp: '-18'
            }, {
                name: 'Sun',
                icon: 'wind',
                highTemp: '23',
                lowTemp: '18'
            }, {
                name: 'Mon',
                icon: 'sleet',
                highTemp: '-1',
                lowTemp: '-6'
            }, {
                name: 'Tue',
                icon: 'clear-day',
                highTemp: '13',
                lowTemp: '7'
            }]
        }
    }
}
</script> 
```
## Props

| Props | Type | Default | Description  |
| --------|:------| -----------|-------|
| units | String | `"us"` | A list of supported units are given below. |
| title | String | `"Weather"` | Title of the widget. |
| enable-credits | Boolean | `true` | Whether or not show dark sky credits |
| current-day | Object | { icon:'clear-night', temp:'23', currentSummary:'Clear.', hourlySummary:'Partly cloudy throughout the night.', windSpeed:5} |  Default values for current day in component
| forecast | Array | [{name: 'Mon', icon: 'clear-day', highTemp: '13', lowTemp: '7'}, ...] | Array of objects representing each day of the forecast|

### Weather icons
List of weather icons: clear-day, clear-night, cloudy, fog, partly-cloudy-day, partly-cloudy-night,
rain, sleet, snow, wind.

### Supported units
List of supported units:    

- `ca`: same as si, except that windSpeed and windGust are in kilometers per hour
- `uk2`: same as si, except that nearestStormDistance and visibility are in miles, and windSpeed and windGust are in miles per hour
- `us`: Imperial units (the default)
- `si`: SI units 

## License 

MIT
