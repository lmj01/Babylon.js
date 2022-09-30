
# 2022-09-27
npm run start
打开dev-watch和tools目录下的babylonServer

开启playground，依赖npm run start中的服务
也是tools目录下的一个server，单独开启server:dev模式


playground中的代码保存时会存入https://snippet.babylonjs.com/中，
返回一个对象，含有snippetIdentifier标识符，用来定位所有的代码内容

snippet服务是一个小server，参考[snippet server reference](https://github.com/BabylonJS/SnippetServerReference/blob/main/index.js)
就是一个读写服务器。