
[![](https://img.shields.io/travis/thiagoh/video-service-url-parser.svg)]((https://github.com/thiagoh/video-service-url-parser/releases/latest))
[![view on npm](http://img.shields.io/npm/v/video-service-url-parser.svg)](https://www.npmjs.org/package/video-service-url-parser)
[![view on github](https://img.shields.io/node/v/video-service-url-parser.svg)](https://github.com/thiagoh/video-service-url-parser)
[![npm](https://img.shields.io/npm/l/video-service-url-parser.svg?style=flat-square)](https://www.npmjs.org/package/video-service-url-parser)
[![npm module downloads](https://img.shields.io/npm/dt/video-service-url-parser.svg)](https://www.npmjs.org/package/video-service-url-parser)

<a name="module_video-service-url-parser"></a>
# Video Services URL Parser

## Supports
- YouTube
- Dailymotion
- Vimeo

FIXME
exports strategy not working

Video Service URL Parser

## Getting Started
### On the server
Install the module with: `npm install video-service-url-parser`

```javascript
var video_service_url_parser = require('video-service-url-parser');
/*
  {
    service: 'youtube',
    videoId: 'uFHIEynduqM'
  }
*/
video_service_url_parser.parse("https://www.youtube.com/watch?v=uFHIEynduqM"); 
```

### In the browser
Download the [production version][min] or the [development version][max].

[min]: https://raw.github.com/thiagoh/video-service-url-parser/master/dist/video-service-url-parser.min.js
[max]: https://raw.github.com/thiagoh/video-service-url-parser/master/dist/video-service-url-parser.js

In your web page:

```html
<script src="dist/video-service-url-parser.min.js"></script>
<script>
/*
  {
    service: 'youtube',
    videoId: 'uFHIEynduqM'
  }
*/
VideoServiceUrlParser("https://www.youtube.com/watch?v=uFHIEynduqM"); 
</script>
```

In your code, you can attach video-service-url-parser's methods to any object.

```html
<script src="dist/video-service-url-parser.min.js"></script>
<script>
/*
  {
    service: 'youtube',
    videoId: 'uFHIEynduqM'
  }
*/
VideoServiceUrlParser('http://www.youtube.com/watch?v=uFHIEynduqM');
</script>
```

## Usage
```html
<script>
/*
  {
    service: 'youtube',
    videoId: 'uFHIEynduqM'
  }
*/
VideoServiceUrlParser('http://www.youtube.com/watch?v=uFHIEynduqM');
VideoServiceUrlParser('http://youtu.be/uFHIEynduqM&foo=bar&fooz=barz');
VideoServiceUrlParser('http://youtube.com/watch?v=uFHIEynduqM&foo=bar&fooz=barz');
VideoServiceUrlParser('http://www.youtube.com/embed/uFHIEynduqM&foo=bar&fooz=barz');

/*
  {
    service: 'vimeo',
    videoId: '43233380'
  }
*/
VideoServiceUrlParser('http://vimeo.com/43233380');
VideoServiceUrlParser('https://www.vimeo.com/43233380?foo=bar&fooz=barz');
</script>
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

_Also, please don't edit files in the "dist" subdirectory as they are generated via Grunt. You'll find source code in the "lib" subdirectory!_

## License
Copyright (c) 2015 Thiago Andrade  
Licensed under the MIT license.
