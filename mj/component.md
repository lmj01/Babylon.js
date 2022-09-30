# Component

Babylon的特征之一就是是ECS(Entity-Component-System实体-组件-系统)，其核心是遵循组合优于继承原则。
以scene场景为单元作为一个实体，每个scene实体包含多个组件。
这样对scene进行解耦，使得每个模块如layers，post-process模块独立性更强。

既然以scene为单元，engine对象也是绑定在scene内部，渲染时不需要通过去调引擎,Mesh对象构造时也是依赖与某个scene的

scene与engine是双向的，scene引用engine，engine引用scene
正是因为这种互相引用，方便了业务层面上的相互应用，避免了全局引用

自v3.1所有场景对象都继承自Node接口，
```js
/**
 * Node is the basic class for all scene objects (Mesh, Light, Camera.)
 */
export class Node implements IBehaviorAware<Node> {
}
```
一般框架中基类会基础事件接口，方便各个部件处理，如three-js中
```js
class Object3D extends EventDispatcher {
}
```

# EventSystem

使用observable观察者模式

## Ammo.js

Ammo.js 使用Emscripten将 Bullet物理引擎 直接移植到JavaScript

## Monaco Editor

monaco基于浏览器，而VSCode基于electron