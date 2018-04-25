# PlantUML

[PlantUML](http://plantuml.com/) 是一个开源项目，支持快速绘制时序图、用例图、类图、活动图、组件图、状态图、对象图、部署图等。同时还支持非 UML 图的甘特图、架构图等。例如下面等用例图：

<div id="xhczgg" data-type="puml" data-display="block" data-align="center" data-src="https://lark-assets-prod.oss-cn-hangzhou.aliyuncs.com/__puml/a7908b49c22b05104624bebc463cd25d.svg" data-width="360" data-height="280" data-text="%40startuml%0A%0Aactor%20A%0Aactor%20B%0A%0AA%20-up-%3E%20(up)%0AA%20-right-%3E%20(center)%0AA%20-down-%3E%20(down)%0AA%20-left-%3E%20(left)%0A%0AB%20-up-%3E%20(up)%0AB%20-left-%3E%20(center)%0AB%20-right-%3E%20(right)%0AB%20-down-%3E%20(down)%0A%0A%40enduml"><img src="https://lark-assets-prod.oss-cn-hangzhou.aliyuncs.com/__puml/a7908b49c22b05104624bebc463cd25d.svg" width="360"/></div>

# 快速入门

在编辑器菜单的实验室中，可以找到 PlantUML 的入口。点击之后会弹出 PlantUML 编辑浮层，在这里你可以参考模板进行修改，然后点击预览即可生成图例了。例如插入下面源码：

```plain
@startuml

actor A
actor B

A -up-> (up)
A -right-> (center)
A -down-> (down)
A -left-> (left)

B -up-> (up)
B -left-> (center)
B -right-> (right)
B -down-> (down)

@enduml
```

就可以生成上面的用例图。

# 更多支持

详见 [http://plantuml.com](http://plantuml.com/)
