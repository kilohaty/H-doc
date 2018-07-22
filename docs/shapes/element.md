# Element (元素)
根元素，被其他元素继承

## 构造方法

#### **constructor(options)**
- 参数
    - {Object} options
    - 属性列表
        
        | 名称         | 类型         | 默认值       | 描述        |
        |-------------|-------------|-------------|-------------|
        | left | `Number` | 0 | 水平方向距离 |
        | top | `Number` | 0 | 垂直方向距离 |
        | angle | `Number` | 0 | 旋转角度 |
        | flipX | `Boolean` | false | 水平翻转 |
        | flipY | `Boolean` | false | 垂直翻转 |
        | visible | `Boolean` | true | 是否可见 |
        
<br>

- 示例

    ```js
      const element = new H.Shapes.Element({
        left: 100,
        top: 50,
        angle: 30,
        flipX: true,
        flipY: false,
        visible: true,
      });
    ```

<br/>

## 方法
#### **set(options)**
设置元素属性

- 参数
    - {Object} options
    - 设置元素的属性
- 示例

    ```js
      element.set({
        left: 20,
        top: 30,
      });
    ```