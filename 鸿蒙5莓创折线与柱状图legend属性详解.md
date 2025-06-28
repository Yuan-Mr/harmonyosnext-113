Hello everyone, welcome back to the special session on HarmonyOS 5 Meichuang chart components. In this episode, we'll explain the detailed usage of the `legend` property in the combined chart component McLineBarChart.  


## 1. `show` Property  
**Function**: Controls whether the legend is displayed.  
**Type**: Boolean  
**Default**: `true`  
**Options**: `true` | `false`  
**Scenario**: Set to `false` to hide the legend.  
**Code Example**:  
```typescript
legend: {
  show: false // Hide the legend
}
```  


## 2. `orient` Property  
**Function**: Sets the arrangement direction of the legend.  
**Type**: String  
**Default**: `'horizontal'`  
**Options**: `'horizontal'` | `'vertical'`  
**Scenario**: Horizontal arrangement suits wide spaces; vertical suits tall spaces.  
**Code Example**:  
```typescript
legend: {
  orient: 'vertical' // Arrange legend vertically
}
```  


## 3. Position Properties  

### 3.1 `left` Property  
**Function**: Sets the left position of the legend.  
**Type**: String | Number  
**Default**: `'auto'`  
**Options**: `'auto'` | `'10%'` | `10`  
**Scenario**: Use to precisely position the left side of the legend.  
**Code Example**:  
```typescript
legend: {
  left: '20%' // 20% from the left edge
}
```  

### 3.2 `right` Property  
**Function**: Sets the right position of the legend.  
**Type**: String | Number  
**Default**: `'auto'`  
**Options**: `'auto'` | `'10%'` | `10`  
**Scenario**: Use to precisely position the right side of the legend.  
**Code Example**:  
```typescript
legend: {
  right: 50 // 50px from the right edge
}
```  

### 3.3 `top` Property  
**Function**: Sets the top position of the legend.  
**Type**: String | Number  
**Default**: `'6%'`  
**Options**: `'auto'` | `'10%'` | `10`  
**Scenario**: Use to precisely position the top of the legend.  
**Code Example**:  
```typescript
legend: {
  top: '10%' // 10% from the top edge
}
```  

### 3.4 `bottom` Property  
**Function**: Sets the bottom position of the legend.  
**Type**: String | Number  
**Default**: `'auto'`  
**Options**: `'auto'` | `'10%'` | `10`  
**Scenario**: Use to precisely position the bottom of the legend.  
**Code Example**:  
```typescript
legend: {
  bottom: 30 // 30px from the bottom edge
}
```  


## 4. Icon Properties  

### 4.1 `icon` Property  
**Function**: Sets the icon shape of legend items.  
**Type**: String  
**Default**: `'roundRect'`  
**Options**: `'rect'` | `'circle'` | `'roundRect'`  
**Scenario**: Choose different icon shapes based on design style.  
**Code Example**:  
```typescript
legend: {
  icon: 'circle' // Use circular icons
}
```  

### 4.2 `iconRadian` Property  
**Function**: Sets the corner radius of rounded rectangles.  
**Type**: Number  
**Default**: `2`  
**Scenario**: Adjust corner radius when `icon` is `'roundRect'`.  
**Code Example**:  
```typescript
legend: {
  icon: 'roundRect',
  iconRadian: 5 // Set larger corner radius
}
```  

### 4.3 `itemWidth` Property  
**Function**: Sets the width of legend icons.  
**Type**: Number  
**Default**: `8`  
**Scenario**: Use to adjust icon width.  
**Code Example**:  
```typescript
legend: {
  itemWidth: 12 // Set wider icons
}
```  

### 4.4 `itemHeight` Property  
**Function**: Sets the height of legend icons.  
**Type**: Number  
**Default**: `8`  
**Scenario**: Use to adjust icon height.  
**Code Example**:  
```typescript
legend: {
  itemHeight: 12 // Set taller icons
}
```  


## 5. Spacing Properties  

### 5.1 `itemGap` Property  
**Function**: Sets the spacing between legend items.  
**Type**: Number  
**Default**: `10`  
**Scenario**: Use to adjust spacing between legend items.  
**Code Example**:  
```typescript
legend: {
  itemGap: 20 // Increase spacing between legend items
}
```  

### 5.2 `itemTextGap` Property  
**Function**: Sets the distance between icons and text.  
**Type**: Number  
**Default**: `5`  
**Scenario**: Use to adjust the distance between icons and text.  
**Code Example**:  
```typescript
legend: {
  itemTextGap: 10 // Increase spacing between icons and text
}
```  


## 6. `align` Property  
**Function**: Sets the alignment of legend markers and text.  
**Type**: String  
**Default**: `'auto'`  
**Options**: `'auto'` | `'left'` | `'right'`  
**Scenario**: Use to manually control the alignment.  
**Code Example**:  
```typescript
legend: {
  align: 'right' // Force right alignment
}
```  


## 7. `selectAble` Property  
**Function**: Sets whether legend items are selectable.  
**Type**: Boolean  
**Default**: `true`  
**Options**: `true` | `false`  
**Scenario**: Set to `false` to disable legend interaction.  
**Code Example**:  
```typescript
legend: {
  selectAble: false // Disable legend selection
}
```  


## 8. `data` Property  
**Function**: Sets legend data.  
**Type**: Array  
**Default**: `[]`  
**Scenario**: Use to customize legend content.  
**Code Example**:  
```typescript
legend: {
  data: ['Sales', 'Inventory', 'Growth Rate'] // Custom legend items
}
```  


## 9. Style Properties  

### 9.1 `textStyle` Property  
**Function**: Sets the default text style of the legend.  
**Type**: Object  
**Sub-properties**:  
- `fontFamily`: Font type (default `'sans-serif'`).  
- `fontWeight`: Font weight (default `'normal'`).  
- `fontSize`: Font size (default `30`).  
- `color`: Font color (default `'#333'`).  
- `formatter`: Text formatting function or string.  

**Code Example**:  
```typescript
legend: {
  textStyle: {
    fontFamily: 'Arial',
    fontSize: 24,
    color: '#666',
    formatter: '{value} Items' // Format text
  }
}
```  

### 9.2 `iconStyle` Property  
**Function**: Sets the default style of legend icons.  
**Type**: Object  
**Scenario**: Use to customize icon styles.  
**Code Example**:  
```typescript
legend: {
  iconStyle: {
    color: '#1890ff', // Icon color
    borderWidth: 1, // Border width
    borderColor: '#333' // Border color
  }
}
```  

### 9.3 `textUnselectedStyle` Property  
**Function**: Sets the text style when legend items are unselected.  
**Type**: Object  
**Sub-properties**:  
- `fontFamily`: Font type (default `'sans-serif'`).  
- `fontSize`: Font size (default `30`).  
- `color`: Font color (default `'#999'`).  

**Code Example**:  
```typescript
legend: {
  textUnselectedStyle: {
    color: '#ccc', // Unselected text color
    fontSize: 20 // Unselected text size
  }
}
```  

### 9.4 `iconUnselectedStyle` Property  
**Function**: Sets the icon style when legend items are unselected.  
**Type**: Object  
**Default**: `{color: '#999'}`  
**Scenario**: Use to customize unselected icon styles.  
**Code Example**:  
```typescript
legend: {
  iconUnselectedStyle: {
    color: '#ddd', // Unselected icon color
    opacity: 0.5 // Unselected icon opacity
  }
}
```  


## 10. Animation Properties  

### 10.1 `animationCurve` Property  
**Function**: Sets the legend animation curve.  
**Type**: String  
**Default**: `'easeOutCubic'`  
**Scenario**: Use to customize animation effects.  
**Code Example**:  
```typescript
legend: {
  animationCurve: 'linear' // Linear animation
}
```  

### 10.2 `animationFrame` Property  
**Function**: Sets the legend animation frame rate.  
**Type**: Number  
**Default**: `0`  
**Scenario**: Use to control animation smoothness.  
**Code Example**:  
```typescript
legend: {
  animationFrame: 30 // Set animation frame rate
}
```  


## 11. `rLevel` Property  
**Function**: Sets the legend rendering level.  
**Type**: Number  
**Default**: `20`  
**Scenario**: Use to adjust the layer relationship between the legend and other elements.  
**Code Example**:  
```typescript
legend: {
  rLevel: 30 // Increase rendering level
}
```  


## Practical Application Case  
The following is a complete `legend` configuration example demonstrating how to use these properties in real projects:  

```typescript
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
    formatter: '{value} Data'
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
  data: ['Sales', 'Profit', 'Growth Rate'],
  selectAble: true,
  animationCurve: 'easeOutQuart',
  animationFrame: 40
}
```  

This configuration achieves:  
1. Horizontally centered legend  
2. Circular icons  
3. Custom text format and color  
4. Different icon colors based on indices  
5. Smooth animation effects  
6. Interactive legend items  


That's all for this episode. We hope this article helps you fully master the usage of the `legend` property in Meichuang's combined chart component. Apply these configurations flexibly in real projects to create beautiful and practical chart effects. If you have any questions, feel free to leave a comment!
