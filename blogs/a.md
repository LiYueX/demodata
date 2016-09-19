# 这里是a页面

```js
function(factory) {

  // Find the global object for export to both the browser and web workers.
  var globalObject = typeof window === 'object' && window ||
                     typeof self === 'object' && self;

  // Setup highlight.js for different environments. First is Node.js or
  // CommonJS.
  if(typeof exports !== 'undefined') {
    factory(exports);
  } else if(globalObject) {
    // Export hljs globally even when using AMD for cases when this script
    // is loaded with others that may still expect a global hljs.
    globalObject.hljs = factory({});

    // Finally register the global hljs with AMD.
    if(typeof define === 'function' && define.amd) {
      define([], function() {
        return globalObject.hljs;
      });
    }
  }
```
|  姓名     |  性别     | 年龄     | 学历     |
| :------------- | :------------- | :------------- | :------------- |
| 李月喜       | 男       | 24       | 本科       |
| 武媛梅      | 女       | 23       | 本科       |
| 颜 朦       | 女       | 23       | 本科       |
