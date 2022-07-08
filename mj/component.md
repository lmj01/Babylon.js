# Component

Babylon的特征之一就是是ECS(Entity-Component-System实体-组件-系统)，其核心是遵循组合优于继承原则。
以scene场景为单元作为一个实体，每个scene实体包含多个组件。
这样对scene进行解耦，使得每个模块如layers，post-process模块独立性更强。

既然以scene为单元，engine对象也是绑定在scene内部，渲染时不需要通过去调引擎