# react-date-range

#WARNING:
###This is a fork from [Adphorus' react-date-range](https://github.com/Adphorus/react-date-range)
###I assume, author does not support his package anymore so I fixed some minor bugs with locales and published it to npm. Feel free to use. All credits goes to [Adphorus](https://github.com/Adphorus).

A React component for choosing dates and date ranges. Uses [Moment.js](http://momentjs.com/) for date operations.

**Live Demo :** [http://adphorus.github.io/react-date-range](http://adphorus.github.io/react-date-range)

![](https://cdn.pbrd.co/images/1fjQlZzy.png)

## Getting Started
### Installation

```
$ npm install --save react-date-range
```

## Usage
### Date Picker
```javascript
import React, { Component } from 'react';
import { Calendar } from 'react-date-range';

class MyComponent extends Component {
	handleSelect(date){
		console.log(date); // Momentjs object
	}

	render(){
		return (
			<div>
				<Calendar
					onInit={this.handleSelect}
					onChange={this.handleSelect}
				/>
			</div>
		)
	}
}

```

###### Available Options (props)
* **date:** *(String, Moment.js object, Function)* - default: today
* **format:** *(String)* - default: DD/MM/YYY
* **firstDayOfWeek** *(Number)* - default: [moment.localeData().firstDayOfWeek()](http://momentjs.com/docs/#/i18n/locale-data/)
* **theme:** *(Object)* see [Demo's source](https://github.com/Adphorus/react-date-range/blob/master/demo/src/components/Main.js#L130)
* **onInit:** *(Function)* default: none
* **onChange:** *(Function)* default: none
* **minDate:** *(String, Moment.js object, Function)* default: none
* **maxDate:** *(String, Moment.js object, Function)* default: none
* **lang:** *(String, 'cn' - Chinese, 'jp' - Japanese, 'fr' - French, 'it' - Italian, 'de' - German, 'es' - Spanish, 'ru' - Russian)* default: none

### Range Picker
```javascript
import React, { Component } from 'react';
import { DateRange } from 'react-date-range';

class MyComponent extends Component {
	handleSelect(range){
		console.log(range);
		// An object with two keys,
		// 'startDate' and 'endDate' which are Momentjs objects.
	}

	render(){
		return (
			<div>
				<DateRange
					onInit={this.handleSelect}
					onChange={this.handleSelect}
				/>
			</div>
		)
	}
}

```

###### Available Options (props)
* **startDate:** *(String, Moment.js object, Function)* - default: today
* **endDate:** *(String, Moment.js object, Function)* - default: today
* **format:** *(String)* - default: DD/MM/YYY
* **firstDayOfWeek** *(Number)* - default: [moment.localeData().firstDayOfWeek()](http://momentjs.com/docs/#/i18n/locale-data/)
* **theme:** *(Object)* see [Demo's source](https://github.com/Adphorus/react-date-range/blob/master/demo/src/components/Main.js#L143)
* **onInit:** *(Function)* default: none
* **onChange:** *(Function)* default: none
* **linkedCalendars:** *(Boolean)* default: false
* **calendars:** *(Number)* default: 2
* **ranges:** *(Object)* default: none
* **minDate:** *(String, Moment.js object, Function)* default: none
* **maxDate:** *(String, Moment.js object, Function)* default: none
* **twoStepChange:** *(Boolean)* default: false
* **rangedCalendars** *(Boolean)* default: false
* **lang:** *(String, 'cn' - Chinese, 'jp' - Japanese, 'fr' - French, 'it' - Italian, 'de' - German, 'es' - Spanish, 'ru' - Russian)* default: none
* **specialDays:** *(Array [{date: Moment.js object}])* default: none
