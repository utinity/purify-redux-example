# purify-redux-example

This is a small redux sample app which demonstrates how domain logic can be written in a pure, self-contained form which is completely decoupled from any framework-dependent code.
* `weather/domain.ts` contains the domain model data structures
* `weather/show-weather-near-me.ts` contains a use case / domain function which locates the users geo position, gets the current temperature for that position and shows it to the user
* `weather/interpreter.ts` is a redux middleware which interprets the domain actions and transforms them into side effects
* `index.ts` creates the redux store and initiates the showWeatherNearMe
* `index.html` contains the view template
* `weather/show-temperature-near-me-impure.ts` is an impure version of the domain function above


## Development Setup
* Install dependencies with `npm install`
* Run `npm start` and open [http://localhost:8080](http://localhost:8080)
* This app uses the [Open Weather Map API](https://openweathermap.org/current). You need to [allow cross-origin requests](https://chrome.google.com/webstore/detail/allow-control-allow-origi/nlfbmbojpeacfghkpbjhddihlkkiljbi) in the browser to make this sample work.
