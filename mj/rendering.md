# Rendering

在RenderingManager类中可以看到至少有四个render group

## RenderingGroup

# Renderer

## EdgesRender

```js
class EdgesRenderer {
    constructor() {
        if (isWebGPU) {
            drawWrapper = new DrawWrapper(engine);
        }
    }
    render() {
        // drawWrapper是处理WebGPU的
        if (drawWrapper) {
            Shader._setDrawWrapper(drawWrapper);
        }
        engine.bindBuffers
        Shader.bind
        engine.drawElementsType
        Shader.unbind
    }
}
// 
```
大致流程还是标准的数据处理

