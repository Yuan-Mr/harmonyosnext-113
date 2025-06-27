大家好，欢迎回来鸿蒙5莓创图表组件的专场，我们这一期来讲解组合图组件McLineBarChart中legend属性的详细用法。

## 1. show属性

作用：控制是否显示图例 类型：Boolean 默认值：true 可选值：true | false 场景：当需要隐藏图例时设置为false 代码示例：

```
legend: {
  show: false // 隐藏图例
}
```

## 2. orient属性

作用：设置图例的排列方向 类型：String 默认值：'horizontal' 可选值：'horizontal' | 'vertical' 场景：横向排列适合空间较宽的场景，纵向排列适合空间较高的场景 代码示例：

```
legend: {
  orient: 'vertical' // 纵向排列图例
}
```

## 3. 位置属性组

### 3.1 left属性

作用：设置图例左侧位置 类型：String | Number 默认值：'auto' 可选值：'auto' | '10%' | 10 场景：需要精确定位图例左侧位置时使用 代码示例：

```
legend: {
  left: '20%' // 距离左侧20%的位置
}
```

### 3.2 right属性

作用：设置图例右侧位置 类型：String | Number 默认值：'auto' 可选值：'auto' | '10%' | 10 场景：需要精确定位图例右侧位置时使用 代码示例：

```
legend: {
  right: 50 // 距离右侧50像素
}
```

### 3.3 top属性

作用：设置图例顶部位置 类型：String | Number 默认值：'6%' 可选值：'auto' | '10%' | 10 场景：需要精确定位图例顶部位置时使用 代码示例：

```
legend: {
  top: '10%' // 距离顶部10%的位置
}
```

### 3.4 bottom属性

作用：设置图例底部位置 类型：String | Number 默认值：'auto' 可选值：'auto' | '10%' | 10 场景：需要精确定位图例底部位置时使用 代码示例：

```
legend: {
  bottom: 30 // 距离底部30像素
}
```

## 4. 图标属性组

### 4.1 icon属性

作用：设置图例项的图标形状 类型：String 默认值：'roundRect' 可选值：'rect' | 'circle' | 'roundRect' 场景：根据设计风格选择不同的图标形状 代码示例：

```
legend: {
  icon: 'circle' // 使用圆形图标
}
```

### 4.2 iconRadian属性

作用：设置圆角矩形的圆角大小 类型：Number 默认值：2 场景：当icon为'roundRect'时，调整圆角大小 代码示例：

```
legend: {
  icon: 'roundRect',
  iconRadian: 5 // 设置较大的圆角
}
```

### 4.3 itemWidth属性

作用：设置图标宽度 类型：Number 默认值：8 场景：需要调整图标宽度时使用 代码示例：

```
legend: {
  itemWidth: 12 // 设置更宽的图标
}
```

### 4.4 itemHeight属性

作用：设置图标高度 类型：Number 默认值：8 场景：需要调整图标高度时使用 代码示例：

```
legend: {
  itemHeight: 12 // 设置更高的图标
}
```

## 5. 间距属性组

### 5.1 itemGap属性

作用：设置图例项之间的间距 类型：Number 默认值：10 场景：需要调整图例项之间的间距时使用 代码示例：

```
legend: {
  itemGap: 20 // 增加图例项间距
}
```

### 5.2 itemTextGap属性

作用：设置图形与文本的距离 类型：Number 默认值：5 场景：需要调整图标与文本之间的距离时使用 代码示例：

```
legend: {
  itemTextGap: 10 // 增加图标与文本间距
}
```

## 6. align属性

作用：设置图例标记和文本的对齐方式 类型：String 默认值：'auto' 可选值：'auto' | 'left' | 'right' 场景：需要手动控制对齐方式时使用 代码示例：

```
legend: {
  align: 'right' // 强制右对齐
}
```

## 7. selectAble属性

作用：设置图例项是否可选 类型：Boolean 默认值：true 可选值：true | false 场景：需要禁用图例交互时设置为false 代码示例：

```
legend: {
  selectAble: false // 禁用图例选择
}
```

## 8. data属性

作用：设置图例数据 类型：Array 默认值：[] 场景：需要自定义图例内容时使用 代码示例：

```
legend: {
  data: ['销量', '库存', '增长率'] // 自定义图例项
}
```

## 9. 样式属性组

### 9.1 textStyle属性

作用：设置图例文字默认样式 类型：Object 子属性：

-   fontFamily：字体类型，默认'sans-serif'
-   fontWeight：字体粗细，默认'normal'
-   fontSize：字体大小，默认30
-   color：字体颜色，默认'#333'
-   formatter：文字格式化函数或字符串

代码示例：

```
legend: {
  textStyle: {
    fontFamily: 'Arial',
    fontSize: 24,
    color: '#666',
    formatter: '{value}项' // 格式化文本
  }
}
```

### 9.2 iconStyle属性

作用：设置图例图标默认样式 类型：Object 场景：需要自定义图标样式时使用 代码示例：

```
legend: {
  iconStyle: {
    color: '#1890ff', // 图标颜色
    borderWidth: 1, // 边框宽度
    borderColor: '#333' // 边框颜色
  }
}
```

### 9.3 textUnselectedStyle属性

作用：设置图例未选中状态的文字样式 类型：Object 子属性：

-   fontFamily：字体类型，默认'sans-serif'
-   fontSize：字体大小，默认30
-   color：字体颜色，默认'#999'

代码示例：

```
legend: {
  textUnselectedStyle: {
    color: '#ccc', // 未选中文字颜色
    fontSize: 20 // 未选中文字大小
  }
}
```

### 9.4 iconUnselectedStyle属性

作用：设置图例未选中状态的图标样式 类型：Object 默认值：{color: '#999'} 场景：需要自定义未选中图标样式时使用 代码示例：

```
legend: {
  iconUnselectedStyle: {
    color: '#ddd', // 未选中图标颜色
    opacity: 0.5 // 未选中图标透明度
  }
}
```

## 10. 动画属性组

### 10.1 animationCurve属性

作用：设置图例动画曲线 类型：String 默认值：'easeOutCubic' 场景：需要自定义动画效果时使用 代码示例：

```
legend: {
  animationCurve: 'linear' // 线性动画
}
```

### 10.2 animationFrame属性

作用：设置图例动画帧数 类型：Number 默认值：0 场景：需要控制动画流畅度时使用 代码示例：

```
legend: {
  animationFrame: 30 // 设置动画帧数
}
```

## 11. rLevel属性

作用：设置图例渲染级别 类型：Number 默认值：20 场景：需要调整图例与其他元素的层级关系时使用 代码示例：

```
legend: {
  rLevel: 30 // 提高渲染级别
}
```

## 实际应用案例

下面是一个完整的legend配置示例，展示了如何在实际项目中使用这些属性：

```
legend: {
  show: true,
  orient: 'horizontal',
  left: 'center',
  top: 'top',
  icon: 'circle',
  itemWidth: 10,
  itemHeight: 10,
  itemGap: 15,
  itemTextGap: 8,
  textStyle: {
    fontFamily: 'Microsoft YaHei',
    fontSize: 24,
    color: '#333',
    formatter: '{value}数据'
  },
  iconStyle: {
    color: function(index) {
      const colors = ['#c23531', '#2f4554', '#61a0a8'];
      return colors[index];
    }
  },
  textUnselectedStyle: {
    color: '#bbb'
  },
  iconUnselectedStyle: {
    color: '#ddd'
  },
  data: ['销售额', '利润', '增长率'],
  selectAble: true,
  animationCurve: 'easeOutQuart',
  animationFrame: 40
}
```

这个配置实现了：

1.  水平居中的图例
1.  圆形图标
1.  自定义的文本格式和颜色
1.  根据索引设置不同的图标颜色
1.  平滑的动画效果
1.  可交互的图例项

好，这期讲到这里就结束了，希望大家通过这篇文章能够全面掌握莓创图表组合图组件中legend属性的使用方法，在实际项目中灵活运用这些配置，创建出美观实用的图表效果。如果有任何问题，欢迎在评论区留言讨论！