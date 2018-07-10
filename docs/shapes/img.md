# Img (图像)
继承于 H.Shapes.Element

## 构造方法

#### **constructor(options)**
- 参数
    - {Object} options
    - 属性列表
        
        | 名称         | 类型         | 默认值       | 描述        |
        |-------------|-------------|-------------|-------------|
        | src | `String` |  | 图像资源路径 |
- 示例

    ```js
      const img = new H.Shapes.Img({
        left: 100,
        top: 50,
        src: 'https://xxx.com/xxx.jpg',
      });
    ```