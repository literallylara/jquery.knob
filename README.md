jquery.knob.js
=============

![](https://i.imgur.com/ct8i6w4.gif)

## Usage

`$(selector).knob({options})`

Options may be provided via `data-` attributes as well
The value of the knobs is presented as normalized percentages (0..1) for type = vol, (-1..+1) for type = pan

## Options

| option           | default  | description |
| ---------------- | -------- | ----------- |
| bgColor        | "#000" | background color of the svg circle the pointer
| fgColor        | "#fff" | color of stroke and knob
| type           | "vol"  | either `"vol"` or `"pan"` |
| tooltip        | true   | show a tooltip while turning indicating the current value, set to "folllow" when you want it to follow the mouse
| turnWith       | null   | the element to apply the rotate transform to as well
| arc            | 360    | the maximum amount of degrees the knob can turn |
| steps          | 100    | the amount of values the button can hold |
| offset         | 0      | angle offset in degrees |
| range          | "auto" | how many pixels the mouse has to move for one rotation ` = element height) |
| invertRange    | false  | whether to invert the direction of rotation when moving the mouse |
| fineTuneFactor | 10     | scales the `range` value when holding down shift
| value          | 0      | the initial value |
| resetValue     | 0      | the value to reset to when double-clicking the knob |
| classPrefix    | "knob" | enables you to chose a different class prefix |

## Events

`grab`, `turn`, `release`, `reset` (should be self-explanatory)  
Each event takes the following paramters: `event`, `value`

## Methods

`$(selector).knob("value" [,newValue])` gets or sets the new value  
`$(selector).knob("destroy")` returns the element to its original state

## Styling

The knob can be styled completely with the following elements:

`.classPrefix-stroke` (svg circle element used to render the stroke)  
`.classPrefix-knob` (does not rotate)  
`.classPrefix-pointer-container` (rotates)  
`.classPrefix-pointer`  
`.classPrefix-tooltip`

When the knob is being turned, the original element also has a `.grab` class.

## Demo

[https://rawgit.com/literallylara/jquery.knob/master/demo.html](https://raw.githubusercontent.com/literallylara/jquery.knob/master/demo.html)