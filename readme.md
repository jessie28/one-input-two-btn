某个应用模块由文本框 input，以及按钮 A，按钮 B 组成。点击按钮 A，会向地址 urlA 发出一个 ajax 请求，并将返回的字符串填充到 input 中（覆盖 input 中原有的数据），点击按钮 B，会向地址 urlB 发出一个 ajax 请求，并将返回的字符串填充到 input 中（覆盖 input 中原有的数据）。


当用户依次点击按钮 A、B 的时候，预期的效果是 input 依次被 urlA、urlB 返回的数据填充，但是由于到 urlA 的请求返回比较慢，导致 urlB 返回的数据被 urlA 返回的数据覆盖了，与用户预期的顺序不一致。


请问如何设计代码，解决这个问题？