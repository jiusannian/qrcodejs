# QRCode.js
QRCode.js is javascript library for making QRCode. QRCode.js supports Cross-browser with HTML5 Canvas and table tag in DOM.
QRCode.js has no dependencies.

## Basic Usages
```
<div id="qrcode"></div>
<script type="text/javascript">
new QRCode(document.getElementById("qrcode"), "http://jindo.dev.naver.com/collie");
</script>
```

or with some options

```
<div id="qrcode"></div>
<script type="text/javascript">
var qrcode = new QRCode(document.getElementById("qrcode"), {
	text: "http://jindo.dev.naver.com/collie",
	width: 128,
	height: 128,
	colorDark : "#000000",
	colorLight : "#ffffff",
	correctLevel : QRCode.CorrectLevel.H
});
</script>
```

and you can use some methods

```
qrcode.clear(); // clear the code.
qrcode.makeCode("http://naver.com"); // make another code.
```

## Browser Compatibility
IE6~10, Chrome, Firefox, Safari, Opera, Mobile Safari, Android, Windows Mobile, ETC.

## License
MIT License

## Contact
twitter @davidshimjs

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/davidshimjs/qrcodejs/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

## option参数说明 
名称 | 默认值|说明
---|---|---
width	|256	|图像宽度
height	|256	|图像高度
typeNumber|	4|	
colorDark	|"#000000"	|前景色
colorLight	|"#ffffff"	|背景色
correctLevel|	QRCode.CorrectLevel.L	|容错级别，可设置为： QRCode.CorrectLevel.L、QRCode.CorrectLevel.M、QRCode.CorrectLevel.Q、 QRCode.CorrectLevel.H


##  api调用 
名称 | 说明
---|---
makeCode(text)	|设置二维码内容
clear()	|清除二维码。（仅在不支持 Canvas 的浏览器下有效）
