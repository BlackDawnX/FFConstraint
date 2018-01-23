# FFConstraint
对 Auto Layout API 进行了简单的封装。

## API
该类的 API 均返回一个 Constraint 数组，这个数组用于视图的 addConstraint 方法添加约束，添加约束时要注意关闭默认的布局方式，否则自动布局将失效，关闭方法：
```
view.translatesAutoresizingMaskIntoConstraints = false
```
### fillScreen
使控件充满父视图
`FFConstraint.fillScreen(item: subView, toItem: superView)`
要注意的是，`toItem` 传入父视图，该方法会返回一个 Constraint 数组，*需要把这个数组传递给父视图的 addConstraint，否则约束不成立。*

### fillOffSet
充满父视图的同时有一定偏移量，用法同上。

### size
约束一个视图的尺寸。
`FFConstraint.size(width: width, height: height, item: item)`

### centerScreen
约束视图使其在父视图居中，注意事项同`fillScreen`

### centerScreenOffSet
约束视图居中并可以有一定偏移。

### topOffSet
约束视图使其距离顶部有一定距离，要使该约束有效，你需要先约束视图的尺寸。
