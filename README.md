[![NPM version][npm-version-image]][npm-url]
[![NPM downloads][npm-downloads-image]][npm-url]
[![MIT License][license-image]][license-url]
[![Build Status](https://travis-ci.org/xch89820/Chart.Funnel.js.svg?branch=master)](https://travis-ci.org/xch89820/Chart.Funnel.js)

# chartjs-plugin-funnel
The funnel plugin for Chart.js > 2.7

## Installation

To download a zip, go to the chartjs-plugin-funnel on Github

To install via npm / bower:

```bash
npm install chartjs-plugin-funnel --save
```

## Usage




To configure the funnel plugin, you can simply set chart type to `funnel`.

Simple example:
```js
var config = {
    type: 'funnel',
    data: {
		datasets: [{
			data: [30, 60, 90],
			backgroundColor: [
				"#FF6384",
				"#36A2EB",
				"#FFCE56"
			],
			hoverBackgroundColor: [
				"#FF6384",
				"#36A2EB",
				"#FFCE56"
			]
		}],
		labels: [
			"Red",
			"Blue",
			"Yellow"
		]
	}
}
```

Funnel chart support upside-down drawing or against left or right side drawing.

Please see `example` folder for more information

![alt tag](https://cloud.githubusercontent.com/assets/4920540/16711980/d7c7a65a-46a9-11e6-94f2-6a3fdc8c79a1.JPG)
![alt tag](https://cloud.githubusercontent.com/assets/4920540/16711969/427ac258-46a9-11e6-8f93-86abf82ed89e.JPG)


You can find documentation for Chart.js at [www.chartjs.org/docs](http://www.chartjs.org/docs).

## Options

#### sort
Reverse or not, you can set 'desc' to draw an upside-down funnel.

default is 'asc'.

#### gap
The gap between to trapezium in our funnel chart. The unit is px.

default is 2

#### keep
Draw element against left or right side.

default is 'auto'.

#### topWidth
The top-width of funnel chart, defualt is 0

#### bottomWidth
The bottom-width of funnel chart, default use the width of canvas.

#### tooltips
The tooltips option is a special option for funnel chart, you should be careful if you want to rewrite the option.

The default option is
```js
{
   callbacks: {
    	title: function (tooltipItem, data) {
			return '';
		},
		label: function (tooltipItem, data) {
			return data.labels[tooltipItem.index] + ': ' + data.datasets[tooltipItem.datasetIndex].data[tooltipItem.index];
		}
	}
}
```
## License

Chart.Funnel.js is available under the [MIT license](http://opensource.org/licenses/MIT).

[license-image]: http://img.shields.io/badge/license-MIT-blue.svg?style=flat
[license-url]: http://opensource.org/licenses/MIT

[npm-url]: https://www.npmjs.com/package/chartjs-plugin-funnel
[npm-version-image]: http://img.shields.io/npm/v/chartjs-plugin-funnel.svg?style=flat

[npm-downloads-image]: http://img.shields.io/npm/dm/chartjs-plugin-funnel.svg?style=flat
