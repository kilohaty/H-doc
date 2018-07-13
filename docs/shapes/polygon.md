# Polygon (多边形)
继承于 H.Shapes.Element

## 构造方法

#### **constructor(options)**
- 参数
    - {Object} options
    - 属性列表
        
        | 名称         | 类型         | 默认值       | 描述        |
        |-------------|-------------|-------------|-------------|
        | points | `Array` | [] | 多边形顶点坐标数组 |
        | lineWidth | `Number` | 1 | 描边线宽 |
        | strokeStyle | `String` | '#000000' | 描边样式 |
        | fillStyle | `String` | 'transparent' | 填充样式 |
<br>

- 示例

    ```js
      const polygon = new H.Shapes.Polygon({
        left: 100,
        top: 50,
        points: [
          {x: 100, y: 0},
          {x: 200, y: 100},
          {x: 0, y: 100},
        ],
        lineWIdth: 2,
        strokeStyle: '#ff0000',
        fillStyle: '#dddddd',
      });
    ```