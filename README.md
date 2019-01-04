# htmlandcss
再次复习一下 html 和 css, js 在下次的计划中。
在 css 中，一个元素的 样式优先 !Import > inline-style > id > class, 并且，在css样式中，浏览器是从上到下去检查， 如果你的元素有两个 class 名，那么不管你的 class名前后关系，而在于 css 中的 上下关系。 另外， {color: red !important;} 这个加了 important 的，将会是第一选择，并且永久是最高的级别，其他的样式都不要了。
## 给css一个自定义的变量名
自定义变量名的方式是 : --variablename, 比如给一只猫的皮肤定义，可以这么用: --cat-skin, 也就是说 有一哥元素是 类名是 随便什么都好，样式是这样的
{--cat-skin: orange;}。  然后你还可以直接用这个 变量给其他要上色的元素使用，比如 某个元素的 background, 你可以这么用这个变量去设置，
h1 的背景， h1 { background: var(--cat-skin); } , 这样，h1 的背景颜色会变成 orange.  另外，如果你的变量值一开始没有设定的话，那就糟糕了，所以，还有更好的用法就是在后面指定一个颜色，如果浏览器没有用你的变量值，就用另一个，很简单，这么用， h1 { background: var(--cat-skin, black) }, 这里面是先查找变量值，如果没有就用后面的 black., 还有如果浏览器不兼容怎么办是吧，在别的浏览器可能无法知道你这个是什么意思，所以为了其他浏览器的兼容，可以在里面写一个一样的 就是这样 h1 { background: red; background: var(--cat-skin); }, 对没错就是两个 background 。 最后，在整个页面中，我们通常是用 :root ,作为一个元素的容器吧，里面可以给自定义变量名，并且赋值，然后这个变量名可以给其他元素使用，
<pre>
<style>
  :root {
      --cat-skin: orange;
      }
  
  h1 {
      background: var(--cat-skin, black);
    }
</style>
</pre>
就像上面的这么设置。如果整个页面的颜色被改变了，你可以在要改变的元素中，直接再重写一遍该属性并且赋值为其他颜色就行了。
## 媒体查询media query
这个是用在 窗口或者其他设备中 更改元素的一些设置，比如下面这个样式。
<pre>
<style>
  :root {
    --penguin-size: 300px;
    --penguin-skin: gray;
    --penguin-belly: white;
    --penguin-beak: orange;
  }
  
  @media (max-width: 350px) {
    :root {
    
      /* 上面的 max-width 设置了 在 350px 宽度下的企鹅样式 */   
      
      --penguin-size: 200px;
      --penguin-skin: black;   
    }
  }
</style>
</pre>
