Simple DateTime Picker For AngularJS
====================================

No JQuery, No Bootstrap, Just AngularJS (ver. 1.3+)

This is taken from https://github.com/kineticsocial/angularjs-datetime-picker

As the main project seems no more maintained, some improvements are done on it for [hesperides](https://github.com/voyages-sncf-technologies/hesperides-gui) project.

You can use this for your needs.

[DEMO](https://rawgit.com/kineticsocial/angularjs-datetime-picker/master/index.html)
[![Imgur](http://i.imgur.com/UJfYMN6.png?1)](https://rawgit.com/kineticsocial/angularjs-datetime-picker/master/index.html)

To Get Started
--------------

For Bower users,

  `$ bower install hesperides-datetime-picker`

1. Include `angularjs-datetime-picker.js` and `angularjs-datetime-picker.css`

        <link rel="stylesheet" href="angularjs-datetime-picker.css" />
        <script src="angularjs-datetime-picker.js"></script>

2. add it as a dependency

        var myApp = angular.module('myApp', ['angularjs-datetime-picker']);

3. Use it

        <input datetime-picker ng-model="model" />

Attributes
------------

  -  date-format: optional, date format e.g. 'yyyy-MM-dd'
  -  year: optional, year selected, e.g. 2015
  -  month: optional, month selected, e.g. 5
  -  day: optional, day selected, e.g. 31
  -  hour: optional, hour selected, 23
  -  minute: optional, minute selected, 59
  -  date-only: optional, if set, timepicker will be hidden
  -  future-only: optional, if set, forces validation errors on dates earlier than now
  -  bind-event: optional, if set, the picker will show when that javascript event occurs, default is 'click' event.

Examples
--------

    <input ng-model="date1" datetime-picker date-only />

    <input ng-model="date1" datetime-picker date-only future-only />

    <input ng-model="date2" bind-event="focus" datetime-picker date-format="yyyy-MM-dd" date-only />

    <input ng-model="date3" datetime-picker date-format="yyyy-MM-dd HH:mm:ss" />

    <input ng-model="date4" datetime-picker hour="23" minute='59'/>

    <input ng-model="date5" datetime-picker date-format="yyyy-MM-dd HH:mm:ss" year="2014" month="12" day="31" />
    
    <input ng-model="date5" datetime-picker date-format="yyyy-MM-dd HH:mm:ss" year="2014" month="12" day="31" bind-event="dblclick"/>
