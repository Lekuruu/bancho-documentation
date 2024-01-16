# ButtonState

This is used inside the [[ReplayFrame]], to tell what keys are being pressed.

| Name   | Value |
| :--:   | :---: |
| None   |   0   |
| Left1  |   1   |
| Right1 |   2   |
| Left2  |   4   |
| Right2 |   8   |

::: info
The button state is bit masked, so that they can be combined into one integer.
:::