# native-lazy-load-image
Native image asynchronous loading lazyLoad, compatible with IE11, suitable for PC, mobile, framework, etc.

## how to use
```js
<script type="text/javascript" src="lazyImg.1.0.0.min.js"></script>
<div class="dom">
  <li>
    <img data-src="image-url" src="demo.jpg" />
  </li>
</div>
<script type="text/javascript">
  const dom = new LazyLoadImg({
    el:document.querySelector('.dom'),
    mode:'default', 
    time:300,
    complete:true, 
    position:{top:0,right:0,bottom:0,left:0},
    before: function(){ },
    success: function(el){ el.classList.add('success');setTimeout(function(){el.classList.remove('success')},1000); },
    error: function (el) { el.src = 'demo.jpg' }
  });
</script>
```
Enjoy!
