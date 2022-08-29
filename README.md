<div align="center">
    <img src="https://github.com/finergyrs/design/blob/master/logos/logo-2019/finergy-charts-logo.png" height="128">
    <a href="https://finergyrs.github.io/charts">
        <h2>Finergy Charts</h2>
    </a>
    <p align="center">
        <p>GitHub-inspired modern, intuitive and responsive charts with zero dependencies</p>
        <a href="https://finergy-rs.fr/charts"> 
            <b>Explore Demos » </b>
        </a>
        <a href="https://codesandbox.io/s/finergy-charts-demo-viqud">
            <b> Edit at CodeSandbox »</b>
        </a>
        <a href="https://finergy-rs.fr/charts/docs">
            <b>Documentation » </b>
        </a>
    </p>
</div>

<p align="center">
    <a href="https://bundlephobia.com/result?p=finergy-charts">
        <img src="https://img.shields.io/bundlephobia/minzip/finergy-charts">
    </a>
</p>

<p align="center">
    <a href="https://finergyrs.github.io/charts">
        <img src=".github/example.gif">
    </a>
</p>

### Contents
* [Installation](#installation)
* [Usage](#usage)
* [Contribute](https://finergy-rs.fr/charts/docs/contributing)
* [License](#license)

#### Installation

##### Via NPM
Install via [`npm`](https://www.npmjs.com/get-npm):

```sh
$ npm install finergy-charts
```

and include in your project:
```js
import { Chart } from "finergy-charts"
```

Or include following for es-modules(eg:vuejs):
```js
import { Chart } from 'finergy-charts/dist/finergy-charts.esm.js'
// import css
import 'finergy-charts/dist/finergy-charts.min.css'
```

##### or include within your HTML

```html
<script src="https://cdn.jsdelivr.net/npm/finergy-charts@1.6.1/dist/finergy-charts.min.umd.js"></script>
<!-- or -->
<script src="https://unpkg.com/finergy-charts@1.6.1/dist/finergy-charts.min.umd.js"></script>
```

#### Usage
```js
const data = {
    labels: ["12am-3am", "3am-6pm", "6am-9am", "9am-12am",
        "12pm-3pm", "3pm-6pm", "6pm-9pm", "9am-12am"
    ],
    datasets: [
        {
            name: "Some Data", chartType: "bar",
            values: [25, 40, 30, 35, 8, 52, 17, -4]
        },
        {
            name: "Another Set", chartType: "line",
            values: [25, 50, -10, 15, 18, 32, 27, 14]
        }
    ]
}

const chart = new finergy.Chart("#chart", {  // or a DOM element,
                                            // new Chart() in case of ES6 module with above usage
    title: "My Awesome Chart",
    data: data,
    type: 'axis-mixed', // or 'bar', 'line', 'scatter', 'pie', 'percentage'
    height: 250,
    colors: ['#7cd6fd', '#743ee2']
})
```

Or for es-modules (replace `new finergy.Chart()` with `new Chart()`):
```diff
- const chart = new finergy.Chart("#chart", {
+ const chart = new Chart("#chart", {  // or a DOM element,
                                    // new Chart() in case of ES6 module with above usage
    title: "My Awesome Chart",
    data: data,
    type: 'axis-mixed', // or 'bar', 'line', 'scatter', 'pie', 'percentage'
    height: 250,
    colors: ['#7cd6fd', '#743ee2']
})
```


If you want to contribute:

1. Clone this repo.
2. `cd` into project directory
3. `npm install`
4. `npm run dev`

#### License
This repository has been released under the [MIT License](LICENSE)

------------------
Project maintained by [Finergy](https://finergy-rs.fr).
Used in [ERPNext](https://erpnext.com). Read the [blog post](https://medium.com/@pratu16x7/so-we-decided-to-create-our-own-charts-a95cb5032c97).
