# Sticky Stack Cards Middle Section Demo

这个示例把错层滚动堆叠卡片完整放入一个中间 section，并在它前后各加入一个普通 section，用于观察页面从上方内容进入堆叠区域、再离开到下方内容时的滚动表现。

## 目录结构

```text
stacked-cards-middle-section/
├── index.html
└── assets/
    ├── css/
    │   └── style.css
    ├── js/
    │   └── main.js
    └── images/
        ├── placeholder-1.svg
        ├── placeholder-2.svg
        ├── placeholder-3.svg
        └── placeholder-4.svg
```

## 核心点

- 上方普通 section：`.page-section--intro`
- 中间堆叠卡片 section：`.page-section--stack.stack-section`
- 下方普通 section：`.page-section--outro`
- 卡片错层依赖：`position: sticky`、`top`、`z-index`
- 中间 section 和父级不能设置 `overflow: hidden`，否则 sticky 可能被裁切或失效。
