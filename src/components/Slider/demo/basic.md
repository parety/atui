---
order: 0
title:
  zh-CN: 按钮类型
  en-US: Type
---

## zh-CN

按钮有四种类型：主按钮、次按钮、幽灵按钮、虚线按钮。

通过设置 `type` 为 `primary` `ghost` `dashed` 可分别创建主按钮、幽灵按钮、虚线按钮，若不设置 `type` 值则为次按钮。不同的样式可以用来区别其重要程度。

主按钮和次按钮可独立使用，幽灵按钮用于和主按钮组合。需要强引导用主按钮，切记主按钮在同一个操作区域最多出现一次。

## en-US


````jsx
basic
<slider :value="30"></slider>
<slider :value="[20,50]"></slider>
<slider :value="[20,50]" disabled></slider>
带有输入框的滑块
<v-row>
  <v-col span="14">
    <slider :value.sync="sliderValue"></slider>
  </v-col>
  <v-col span="10">
    <v-input type="text" :value.sync="sliderValue"></v-input>
  </v-col>
</v-row>
有取值区间的滑块
<slider :value="1" :min="1" :max="21"></slider>
````

````vue-script
new Vue({
    el: 'body',
    components: {
        slider: atui.Slider,
        vRow: atui.Layout.Row,
        vCol: atui.Layout.Col,
        vInput: atui.Input
    }
})
````