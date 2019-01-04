# htmlandcss
再次复习一下 html 和 css, js 在下次的计划中。
在 css 中，一个元素的 样式优先 !Import > inline-style > id > class, 并且，在css样式中，浏览器是从上到下去检查， 如果你的元素有两个 class 名，那么不管你的 class名前后关系，而在于 css 中的 上下关系。 另外， {color: red !important;} 这个加了 important 的，将会是第一选择，并且永久是最高的级别，其他的样式都不要了。
## 给css一个自定义的变量名
自定义变量名的方式是 : --variablename, 比如给一只猫的皮肤定义，可以这么用: --cat-skin, 也就是说 有一哥元素是 类名是 随便什么都好，样式是这样的
{--cat-skin: orange;}
