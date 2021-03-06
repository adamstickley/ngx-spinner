<p align="center">
  <img height="200px" width="200px" style="text-align: center;" src="https://cdn.rawgit.com/Napster2210/ngx-spinner/gh-pages/assets/logo.png">
  <h1 align="center">NgxSpinner</h1>
</p>

A library for loading spinner specifically for Angular 4/5/6/7. (https://napster2210.github.io/ngx-spinner/)

[![ng5](https://img.shields.io/travis/rust-lang/rust.svg?style=flat-square)]()
[![Support](https://img.shields.io/badge/Support-Angular%204%2B-blue.svg?style=flat-square)]()
[![Support](https://img.shields.io/badge/Support-Angular%205%2B-blue.svg?style=flat-square)]()
[![Support](https://img.shields.io/badge/Support-Angular%206%2B-blue.svg?style=flat-square)]()
[![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)]()
[![devDependency Status](https://img.shields.io/david/expressjs/express.svg?style=flat-square)]()

## What's New

- Multiple Spinner Support
- Configurable option through service
- Latest update for **Angular 7** 🎉🎉🥳🥳
- Fullscreen Mode(Enable/Disable)

The version 1.x supports Angular 4. <b>UPDATE: Now works with Angular 4(v1.2.0)</b>

| Angular 4 | Angular 5 | Angular 6/7
| --- | --- | --- |
| >= `v1.2.0` | >= `v2.0.0` | >= `v7.0.0` |

## Table of contents

- [Browser Support](#browser-support)
- [Demo](#demo)
- [Installation](#installation)
- [Usage](#usage)
- [Versioning](#versioning)
- [Creator](#creator)
- [Future Plan](#future-plan)
- [Credits](#credits)
- [License](#license)

## Browser Support

![Chrome](http://icons.iconarchive.com/icons/google/chrome/48/Google-Chrome-icon.png) | ![Firefox](https://support.cdn.mozilla.net/static/sumo/img/favicon.ico) | ![IE](https://www.msccruises.co.uk/wcsstore/MSCB2CStoreFrontAssetStore//images/icon_ie.png) | ![Safari](https://aplweb.sercomtel.com.br/sistemas/areaCliente/img/logoSafari.png) | ![Opera](https://www.webcomponents.org/assets/opera.png)
--- | --- | --- | --- | --- |
Latest ✔ | Latest ✔ | 10+ ✔ | Latest ✔ | Latest ✔ |

## Demo

[Working Demo](https://napster2210.github.io/ngx-spinner/)
- More working example for coming soon(stackblitz)...

## Installation

`ngx-spinner` is available via [npm](https://www.npmjs.com/package/ngx-spinner) and [yarn](https://yarnpkg.com/en/package/ngx-spinner)

Using npm:
```bash
$ npm install ngx-spinner --save
```

Using yarn:
```bash
$ yarn add ngx-spinner
```

## Usage

Import `NgxSpinnerModule` in  in the root module(`AppModule`):
```typescript
// Import library module
import { NgxSpinnerModule } from 'ngx-spinner';

@NgModule({
  imports: [
    // ...
    NgxSpinnerModule
  ]
})
export class AppModule { }
```

Add `NgxSpinnerService` service wherever you want to use the `ngx-spinner`.
```typescript
import { NgxSpinnerService } from 'ngx-spinner';

class AppComponent implements OnInit {
  constructor(private spinner: NgxSpinnerService) { }

  ngOnInit() {
    /** spinner starts on init */
    this.spinner.show();

    setTimeout(() => {
        /** spinner ends after 5 seconds */
        this.spinner.hide();
    }, 5000);
  }
}
```

Now use in your template
```html
<ngx-spinner></ngx-spinner>
```
See [Demo](#demo)

## NgxSpinner Service

- `NgxSpinnerService.show()`  Shows the spinner
- `NgxSpinnerService.hide()`  Hides the spinner

## NgxSpinner Component

```html
<ngx-spinner
  bdColor="rgba(51,51,51,0.8)"
  size="medium"
  color="#fff"
  type="ball-scale-multiple">
 <p style="font-size: 20px; color: white">Loading...</p>
</ngx-spinner>
```

- **[bdColor]**: RGBA color format.
  To set background-color for backdrop, default `rgba(51,51,51,0.8)` where `aplha` value(0.8) is opacity of backdrop
- **[size]**: Anyone from `small`, `default`, `medium`, `large`.
  To set size of spinner, default `large`
- **[color]**: Any css color format.
  To set color of spinner, default `#fff`
- **[type]**: Choose any animation spinner from [Load Awesome](http://github.danielcardoso.net/load-awesome/animations.html).
  To set type of spinner, default `ball-scale-multiple`
- **[fullScreen]**: `true` or `false`
To enable/disable fullscreen mode(overlay), default `true`
---
#### NOTE: 
- You can pass `HTML` code as loading text now, instead of input parameter(`loadingText`). Check above code for reference.
- If you want multiple `ngx-spinner` instance fro multiple spinner support, just add `name` attribute with `ngx-spinner` component.But in this case, in `show/hide` method you've to pass that particular name of spinner. Check [Demo](#demo)
- You can also change the options/configuration of spinner through service now.
```javascript
this.spinner.show('mySpinner', {
  type: 'line-scale-party', 
  size: 'large', 
  bdColor: 'rgba(100,149,237, .8)', 
  color: 'white'
});
```

### How to use type?

- Go to the [Load Awesome](http://github.danielcardoso.net/load-awesome/animations.html).
- Select any animation, copy name of animation, replace all spaces with hyphen(-) and all letters should be lowercase.
  - Let's say if I select "Ball 8bits" animation then `type` will be `ball-8bits`.
  - For more information you can check it out [Demo](https://napster2210.github.io/ngx-spinner/)


## Versioning

ngx-spinner will be maintained under the Semantic Versioning guidelines.
Releases will be numbered with the following format:

`<major>.<minor>.<patch>`

For more information on SemVer, please visit http://semver.org.

## Creator

#### [Yuvraj Chauhan](mailto:yuvrajchauhan3113@gmail.com)
- [@GitHub](https://github.com/Napster2210)

## Future Plan

- Interceptor Implementation (Coming soon)

## Credits

 Inspired by [Load Awesome by Daniel Cardoso.](https://github.com/danielcardoso/load-awesome)
 
 Thanks [Alex Vieira Alencar](https://github.com/iamavieira) for Multiple Spinner Support

## License

#### The MIT License (MIT)
