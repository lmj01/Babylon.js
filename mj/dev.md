
# dev
npm run start
打开dev-watch和tools目录下的babylonServer

开启playground，依赖npm run start中的服务
也是tools目录下的一个server，单独开启server:dev模式

## tools

### babylonServer

### playground

playground中的代码保存时会存入https://snippet.babylonjs.com/中，返回一个对象，含有snippetIdentifier标识符，用来定位所有的代码内容, 
playground中的examples是通过https://babylonjs-newdocs.search.windows.net的一个接口返回文档中的snippet内容

snippet服务是一个小server，参考[snippet server reference](https://github.com/BabylonJS/SnippetServerReference/blob/main/index.js)
就是一个读写服务器。

### devHost
简单的一个基本场景加载逻辑，通过创建一个scene函数来运行，可以定制scene代码的逻辑