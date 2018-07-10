# RegularPolygon (正多边形)
继承于 H.Shapes.Polygon

## 构造方法

#### **constructor(options)**
- 参数
    - {Object} options
    - 属性列表
        
        | 名称         | 类型         | 默认值       | 描述        |
        |-------------|-------------|-------------|-------------|
        | edgeNumber | `Number` | 3 | 边数量 |
        | radius | `Number` | 0 | 外切圆半径 |
        | startAngle | `Number` | 0 | 起始角度 |
- 示例

    ```js
      const regularPolygon = new H.Shapes.RegularPolygon({
        left: 100,
        top: 50,
        edgeNumber: 5,
        radius: 100,
        startAngle: 45,
        lineWidth: 2,
        strokeStyle: '#ff0000',
        fillStyle: '#dddddd',
      });
    ```

