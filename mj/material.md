# Material

## Effect
Effect containing vertex and fragment shader that can be executed on an object
```js
class Effect {
    constructor() {
        this._processingContext = this._engine._getShaderProcessingContext(this._shaderLanguage);
    }
}

```

## Node Material

### NMD(Node Material Decorator)
节点材质装饰器
