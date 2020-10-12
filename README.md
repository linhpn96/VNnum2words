<div align="center" markdown="1">

# VNnum2words.js
**Vietnamese convert number to words by js(chuyển số thành chữ trong tiếng việt bằng ngôn ngũ javascript)**

</div>


## installation

In a browser(trong trình duyệt):
```html
normal script(dùng javascript thông thường):
<script src="https://cdn.jsdelivr.net/gh/linhpn96/VNnum2words/src/index.js">

module script( dùng cho module):
<script type="module">
    import {default as VNnum2words} from 'https://cdn.jsdelivr.net/gh/linhpn96/VNnum2words/src/index.mjs';
</script>

```

Using npm:
```shell
$ npm i -g npm
$ npm i vn-num2words
```
Note: add `--save` if you are using npm < 5.0.0

In Node.js(trong nodejs):
```
//js
const VNnum2words = require('vn-num2words');
console.log(VNnum2words(10000));
//es module
import {default as VNnum2words} from 'vn-num2words';
console.log(VNnum2words(10000));
```

In es6 babel
```
import VNnum2words from 'vn-num2words';
console.log(VNnum2words(10000));

```
## warning
in javascript the number type is corrected true is less than 9007199254740991 so if number greater than 9007199254740991 must use string, or you can use string for all case
trong javascript định dạng số bị giới hạn ở 9007199254740991 nên nếu số lớn hơn 9007199254740991 mời dùng kiểu chuỗi, hoặc là dùng toàn bộ là string
## example

```
less than 9007199254740991:
VNnum2words(1000001);
greater than 9007199254740991:
VNnum2words('1234567899876543210101'));
or use tring all case
VNnum2words('100'));


0 không
1 một
10 mười
14 muời bốn
100 một trăm
101 một trăm linh một
125 một trăm hai mươi lăm
1000 một nghìn
100000 một trăm nghìn
1000001 một triệu không nghìn không trăm linh một
1000000000000000001 một tỷ tỷ không trăm linh một
123450000000000001 một trăm hai mươi ba triệu bốn trăm năm mươi nghìn tỷ không trăm linh một
123450000001 một trăm hai mươi ba tỷ bốn trăm năm mươi triệu không nghìn không trăm linh một
1234567899876543210101 một nghìn hai trăm ba mươi tư tỷ  tỷ năm trăm sáu mươi bẩy triệu tám trăm chín mươi chín nghìn tám trăm bẩy mươi sáu tỷ năm trăm bốn mươi ba triệu hai trăm mười nghìn một trăm linh một


```