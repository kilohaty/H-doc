# Text (文本)
继承于 H.Shapes.Element

## 构造方法

#### **constructor(options)**
- 参数
    - {Object} options
    - 属性列表
        
        | 名称         | 类型         | 默认值       | 描述        |
        |-------------|-------------|-------------|-------------|
        | text | `String` |  | 文本内容 |
        | fontSize | `Number` | 12 | 字号 |
        | textAlign | `String` | left | 文本对齐方式 |
        | textBaseLine | `String` | top | 文本基线 |
        | fillStyle | `String` | #000 | 文本样式 |
        
<br>

- 示例

    ```js
      const text = new H.Shapes.Text({
        left: 100,
        top: 50,
        text: 'HRender 文本',
        fontSize: 36,
        fillStyle: '#ff0000'
      });
    ```