# angularWx

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 15.0.4 and is based on the YouTube video found at: https://www.youtube.com/watch?v=psZXU8PTAS8.

The API in the video no longer works as shown and I updated the code to work with weatherAPI through [RapidAPI](https://rapidapi.com/weatherapi/api/weatherapi-com/) as the format is similar. You can see the API code in the `src/environments/environment.example.ts` file. 

I also changed the .upper-data block background image to reflect the day/night cycle (`*ngIf="weatherData.current.is_day == 1"` and `*ngIf="weatherData.current.is_day == 0"`) instead of a temperature based hot/cold indicator (`*ngIf="weatherData.current.temp_f > 60"` and `*ngIf="weatherData.current.temp_f <= 59"`).

Another change made is to display all values in the imperial format (`weatherData.current.temp_f` vs `weatherData.current.temp_c` and `weatherData.current.wind_mph` vs `weatherData.current.wind_kph`) and the default city is set to San Antonio.

Also, I set up a static version of the page that shows if the API call fails (`*ngIf="!weatherData"` in the second container div.) and there is no valid available data. There is a text phrase that shows up indicating that the data is not current. 

Lastly, I removed the console log of the repsonse that was in the `app.component.ts` file. If you are having API issues, you may want to add it back to aid in troubleshooting.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
