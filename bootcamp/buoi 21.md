# Bootcamp - Buổi 18

## DOM và Events Fundamentals
### 1. DOM là gì? 
- DOM giúp cho bạn có thể truy cập và thay đổi các elements trong HTML document
- Khi bạn truy cập vào một trang web, website khi load xong thì trình duyệt sẽ tạo cho bạn một DOM (Document Object Model)

![](https://i.imgur.com/qrFwV9g.png)

- Lúc này bạn có thể tạo ra được một dynamic HTML:
	- JS có thể thay đổi HTML elements (Update, Thêm, Xoá)
	- JS có thể thay đổi HTML attributes (src, height, width)
	- JS có thể thay đổi CSS styles
	- JS có thể react tới các events HTML


- DOM là một chuẩn của W3C
- Tiêu chuẩn W3C DOM được chia thành 3 phần khác nhau:
	- Core DOM - standard model for all document types
	- XML DOM - standard model for XML documents
	- HTML DOM - standard model for HTML documents

### 2. DOM methods
- Phương thức DOM là những **actions** bạn có thể làm trên HTML elements (Thêm, xoá, sửa)
- Thuộc tính DOM là những giá trị bạn có thể set và thay đổi

#### 2.1 DOM Programming Interface
- DOM có thể truy cập với Javascript
- HTML elements trong DOM sẽ được định nghĩa như là object trong Javascript

Ví dụ, bạn có thể thay đổi content bên trong `<p id="demo"></p>`

```html
<html>  
<body>  
	<p id="demo"></p>  
	<script>  
	document.getElementById("demo").innerHTML = "Hello World!";  
	</script>  
</body>  
</html>
```

Ở ví dụ trên, `getElementById("demo")` là một phương thức, `innerHTML` là một thuộc tính

#### 2.2 The getElementById Method

- Phương thức được sử dụng phổ biến nhất là `getElementById` 
- Trong trường hợp trên, `getElementById` sử dụng `id=demo` để tìm ra element đó


#### 2.3 The innerHTML Property

- Cách đơn giản nhất để lấy nội dung của elements là sử dụng `innerHTML`
- `innerHTML`  là thuộc tính có ích cho việc lấy và thay thế nội dung của elements

### 3. DOM Document

#### 3.1 DOM Document Object
- DOM document object đại diện cho website của bạn
- Nếu bạn muốn truy cập bất kì các element nào trong HTML page, thì bạn luôn luôn bắt đầu với document object

#### 3.2 Finding HTML Elements

![](https://i.imgur.com/iVsOltD.png)

 - Finding HTML Elements by CSS Selectors
	- If you want to find all HTML elements that match a specified CSS selector (id, class names, types, attributes, values of attributes, etc), use the `querySelectorAll()` method.

```js
const x = document.querySelectorAll("p.intro");
```

#### 3.3 Changing HTML Elements
![](https://i.imgur.com/tlLyD43.png)


#### 3.4 Add and Delete Elements

![](https://i.imgur.com/hx7lQXF.png)

#### 3.5 Adding Events Handlers
![](https://i.imgur.com/suWWzvp.png)

#### 3.6 Finding HTML Objects

```js
document.body      // Returns the <body> element
document.baseURI   // Returns the absolute base URI of the document
document.domain    // Returns the domain name of the document server
document.title     // Returns the <title> element
document.URL       // Returns the complete URL of the document
```


### 4. DOM Elements
- Cách để tìm và truy cập một HTML elements trong HTML page
	-   Finding HTML elements by id
	-   Finding HTML elements by tag name
	-   Finding HTML elements by class name
	-   Finding HTML elements by CSS selectors
	-   Finding HTML elements by HTML object collections

#### Finding HTML elements by id
- Đây là cách dễ nhất để tìm một element trong HTML 

```js
const element = document.getElementById("intro");
```

- Nếu element được tìm ra, thì phương thức này sẽ trả lại cho bạn element như là object
- Ngược lại, nếu không tìm ra thì nó sẽ trả lại cho bạn `null`


#### Finding HTML Elements by Tag Name

```js
const element = document.getElementsByTagName("p");
```

Ví dụ dưới đây tìm elements với `id="main"` và sau đó tìm tất cả thẻ `p` bên trong `main`
```js
const x = document.getElementById("main");  
const y = x.getElementsByTagName("p");
```

#### Finding HTML Elements by Class Name
- Nếu bạn muốn tìm HTML elements thông qua class name, thì sử dụng `getElementsByClassName()`

- Ví dụ dưới đây sẽ trả lại cho bạn list của tất cả các element có `class="intro"`
```js
const x = document.getElementsByClassName("intro");
```

#### Finding HTML Elements by CSS Selectors
- Nếu bạn muốn tìm tất cả HTML elements mà match với CSS selector (id, class names, types, attributes, values of attributes), sử dụng phương thức `querySelectorAll()`
- Ví dụ dứoi đây trả lại cho bạn list của tất cả thẻ `p` với `class="intro"`

```js
const x = document.querySelectorAll("p.intro");
```

#### Finding HTML Elements by HTML Object Collections
- This example finds the form element with `id="frm1"`, in the forms collection, and displays all element values:

```js
const x = document.forms["frm1"];  
let text = "";  
for (let i = 0; i < x.length; i++) {  
  text += x.elements[i].value + "<br>";  
}  
document.getElementById("demo").innerHTML = text;
```

The following HTML objects (and object collections) are also accessible:
-   [document.anchors](https://www.w3schools.com/js/tryit.asp?filename=tryjs_doc_anchors)
-   [document.body](https://www.w3schools.com/js/tryit.asp?filename=tryjs_doc_body)
-   [document.documentElement](https://www.w3schools.com/js/tryit.asp?filename=tryjs_doc_element)
-   [document.embeds](https://www.w3schools.com/js/tryit.asp?filename=tryjs_doc_embeds)
-   [document.forms](https://www.w3schools.com/js/tryit.asp?filename=tryjs_doc_forms)
-   [document.head](https://www.w3schools.com/js/tryit.asp?filename=tryjs_doc_head)
-   [document.images](https://www.w3schools.com/js/tryit.asp?filename=tryjs_doc_images)
-   [document.links](https://www.w3schools.com/js/tryit.asp?filename=tryjs_doc_links)
-   [document.scripts](https://www.w3schools.com/js/tryit.asp?filename=tryjs_doc_scripts)
-   [document.title](https://www.w3schools.com/js/tryit.asp?filename=tryjs_doc_title)


### 5. DOM HTML
- HTML DOM cho phép bạn có thể thay đổi nội dung của HTML elements

#### Changing HTML Content
- Cách đơn giản nhất để thay đổi nội dung của HTML element là sử dụng `innerHTML` property
- Ví dụ dưới đây thay đổi nội dung của `p` element

```html
<html>  
	<body>  
		<p id="p1">Hello World!</p>  
		<script>  
			document.getElementById("p1").innerHTML = "New text!";  
		</script>  
	</body>  
</html>
```

- Giải thích:
	- HTML trên chứa đựng thẻ `p` với `id=p1`
	- Chúng ta sẽ sử dụng HTML DOM để lấy element với `id="p1"`
	- JS thay đổi nội dung (`innerHTML`) của element đó thành `New text!`

#### Changing the Value of an Attribute
- Để thay đổi gía trị của attribute (property) của một element, sử dụng cú pháp:

```txt
document.getElementById(id).attribute = new value
```

Ví dụ dứoi đây thay đổi giá trị của `src`  attribute của một thẻ `img`

```html
<!DOCTYPE html>  
<html>  
	<body>  
		  
		<img id="myImage" src="smiley.gif">  
		  
		<script>  
			document.getElementById("myImage").src = "landscape.jpg";  
		</script>  
	  
	</body>  
</html>
```

- Giải thích:
	- HTML trên chứa đựng thẻ `img` với `id=myImage`
	- Chúng ta sẽ sử dụng HTML DOM để lấy element với `id="myImage"
	- JS thay đổi `src`của element từ `"smiley.gif"` đó thành `"landscape.jpg"`


#### Dynamic HTML content
- Bạn có thể tạo ra một nội dung HTML động

```html
<!DOCTYPE html>  
<html>  
	<body>  
	  
	<script>document.getElementById("demo").innerHTML = "Date : " + Date(); </script>  
	  
	</body>  
</html>
```


#### document.write()
- Trong javascript, `document.write()` được sử dụng để viết trực tiếp đến HTML output stream
```js
<!DOCTYPE html>  
<html>  
	<body>  
	  
		<p>Bla bla bla</p>  
		  
		<script>  
			document.write(Date());  
		</script>  
		  
		<p>Bla bla bla</p>  
	  
	</body>  
</html>
```




### 6. DOM Forms
#### JavaScript Form Validation
- HTML Form validation có thể được hoàn thành bởi Javascript
- Nếu một form field bị empty (trống), function này gửi message cảnh báo, và return false, để ngăn chặn form từ việc submit

```js
function validateForm() {  
  let x = document.forms["myForm"]["fname"].value;  
  if (x == "") {  
    alert("Name must be filled out");  
    return false;  
  }  
}
```

- Function sẽ được gọi khi form được submit

```html
<form name="myForm" action="/action_page.php" onsubmit="return validateForm()" method="post">  
Name: <input type="text" name="fname">  
<input type="submit" value="Submit">  
</form>
```

#### JavaScript Can Validate Numeric Input
- JS thường được sử dụng để validate numeric input

```html
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Validation</h2>

<p>Please input a number between 1 and 10:</p>

<input id="numb">

<button type="button" onclick="myFunction()">Submit</button>

<p id="demo"></p>

<script>
function myFunction() {
  // Get the value of the input field with id="numb"
  let x = document.getElementById("numb").value;
  // If x is Not a Number or less than one or greater than 10
  let text;
  if (isNaN(x) || x < 1 || x > 10) {
    text = "Input not valid";
  } else {
    text = "Input OK";
  }
  document.getElementById("demo").innerHTML = text;
}
</script>

</body>
</html> 
```

![](https://i.imgur.com/57gT2tC.png)


#### Automatic HTML Form Validation

- HTML Form Validation được thực hiện tự động bởi trình duyệt
- Nếu một form field bị empty, `required` attribute sẽ ngăn chặn form này submit:
```html
<form action="/action_page.php" method="post">  
  <input type="text" name="fname" required>  
  <input type="submit" value="Submit">  
</form>
```

**Note**: Automatic HTML form validation does not work in Internet Explorer 9 or earlier.

#### Data Validation
- Data Validation là quá trình đảm bảo user input luôn clean, correct và useful
- Các loại validation điển hình:
	- User đã fill hết tất cả fields chưa?
	- User đã nhập đúng valid date?
	- User nhập text trong numeric field?

- Thông thường, mục đích của data validation là đảm bảo correct user input
- Validation có thể được định nghĩa theo nhiều cách khác nhau, và triển khai theo nhiều cách khác nhau
- **Server side validation** được thực hiện bởi web server, sau khi input được gửi tới server
- **Client side validation** được thực hiện bởi web browser, trước khi input được gửi tới server


#### HTML Constraint Validation
HTML5 giới thiệu một concept mới là HTML validation được gọi là constraint validation
HTML Constraint Validation dựa vào:
- **HTML Input Attributes**
- **CSS Pseudo Selectors**
- **DOM Properties and Methods**

#### Constraint Validation HTML Input Attributes
![](https://i.imgur.com/vN2X50c.png)

#### Constraint Validation CSS Pseudo Selectors
![](https://i.imgur.com/6xjjWX4.png)


### 7. DOM CSS
HTML DOM cho phép JS thay đổi style của HTML elements

#### Changing HTML Style
```
document.getElementById(_id_).style._property_ = _new style_
```

Ví dụ dưới đây thay đổi style của thẻ `p`:
```html
<html>  
<body>  
  
<p id="p2">Hello World!</p>  
  
<script>  
document.getElementById("p2").style.color = "blue";  
</script>  
  
</body>  
</html>
```

#### Using Events
HTML DOM cho phép các bạn thực thi code khi một event xảy ra
Các event được tạo ra bởi browser khi "things happen" với HTML elements:
-  Element được click
-  Page đã load
-  Input field được thay đổi

Ví dụ dứoi đây thay đổi style của HTML element với `id="id1"`, khi user click một button:
```html
<!DOCTYPE html>  
<html>  
<body>  
  
<h1 id="id1">My Heading 1</h1>  
  
<button type="button"  
onclick="document.getElementById('id1').style.color = 'red'">  
Click Me!</button>  
  
</body>  
</html>
```




### 8. DOM Events
- HTML DOM cho phép Javascript tương tác với HTML events


#### React to Events
- JS được thực thi khi một sự kiên xảy ra, ví dụ user click vào một HTML element
- Để thực thi code khi user click vào một element, thêm JS code đến một HTML event attribute:

```txt
onclick=_JavaScript_
```

Ví dụ về HTML elements:
- Khi user click mouse
- Khi website load xong
- Khi hình ảnh load xong
- Khi mouse hover trên element
- Khi input field được thay đổi
- Khi HTML form được submit
- Khi user gõ nút bàn phím

Ví dụ, thay đổi content của thẻ `h1` khi user click vào nó
```html
<!DOCTYPE html>  
<html>  
<body>  
  
<h1 onclick="this.innerHTML = 'Ooops!'">Click on this text!</h1>  
  
</body>  
</html>
```

Trong ví dụ này, function được gọi từ event handler
```html
<!DOCTYPE html>  
<html>  
<body>  
  
<h1 onclick="changeText(this)">Click on this text!</h1>  
  
<script>  
function changeText(id) {  
  id.innerHTML = "Ooops!";  
}  
</script>  
  
</body>  
</html>
```


#### HTML Event Attributes
- Để chỉ định events cho HTML element bạn có thể sử dụng event attributes

- Chỉ định onlick event cho button element
```html
<button onclick="displayDate()">Try it</button>
```

Trong ví dụ trên, `displayDate()` sẽ được gọi khi user click vào button

#### Assign Events Using the HTML DOM
- HTML DOM cho phép bạn chỉ định event đến một HTML element sử dụng JS:

- Chỉ định onclick event cho button element
```html
<script>  
document.getElementById("myBtn").onclick = displayDate;  
</script>
```

- Trong ví dụ trên, function `displayDate` được chỉ định đến HTML element với `id="myBtn"`
- Function sẽ được thi thi khi các bạn click vào button

#### The onload and onunload Events
- `onload` và `onunload` được kích hoạt khi user vào hoặc rời một trang web
- `onload` được sử dụng để kiểm tra loại browser và version browser của visitor, và load version phù hợp của trang web dựa vào thông tin
- `onload` và `onunload`  được sử dụng để làm việc với cookies

```html
<body onload="checkCookies()">
```

#### The onchange Event
- `onchange` thường được sử dụng trong kết hợp với validation của input field
- Ví dụ dứoi đây sử dụng event `onchange`. Function `upperCase` được gọi khi mà user thay đổi nội dung của input field

```html
<input type="text" id="fname" onchange="upperCase()">
```

#### The onmouseover and onmouseout Events
- Giống như hover trong CSS
- `onmouseover` và `onmouseout` events được sử dụng để kích hoạt function khi user di chuyển chuột vào hoặc di chuyển ra element

#### The onmousedown, onmouseup and onclick Events
- `onmousedown`, `onmouseup`, `onclick` event là tất cả phần trong mouse-click.
- Đâu tiên khi mouse button được click và `onmousedown` sẽ được kích hoạt, sau đó, khi mouse button được released (bỏ ra), `onmousedown` sẽ được kích hoạt, cuối cùng mouse click được hoàn thành, `onclick` event được kích hoạt

Ví dụ:
[onmousedown and onmouseup](https://www.w3schools.com/js/tryit.asp?filename=tryjs_event_onmousedown)  
Change an image when a user holds down the mouse button.

[onload](https://www.w3schools.com/js/tryit.asp?filename=tryjs_event_onload)  
Display an alert box when the page has finished loading.

[Mouse Events](https://www.w3schools.com/js/tryit.asp?filename=tryjs_event_onmouse)  
Change the color of an element when the cursor moves over it


- List của các HTML DOM events: [HTML DOM Event Object Reference](https://www.w3schools.com/jsref/dom_obj_event.asp).

### 9. DOM Event Listener

#### The addEventListener() method

- Thêm một event listener khi user click vào button

```js
document.getElementById("myBtn").addEventListener("click", displayDate);
```

- `addEventListener()` đính kèm event handler đến một element
- `addEventListener()` đính kèm event handler đến một element mà không overwrite event handler đang tồn tại
- Bạn có thể thêm event handler cho 1 element
- Bạn có thể thêm event handler với cùng type cho một element, i.e two "click" events
- Bạn có thể thêm event listeners cho bất kỳ DOM object không chỉ HTML elements. i.e window object
- `addEventListener()` làm nó dễ kiểm soát cách event phản ứng với bubbling
- Khi sử dụng `addEventListener()`, JS sẽ tách từ HTML markup, tốt cho việc đọc code và cho phép bạn thêm event listeners thậm chí khi bạn không kiểm soát HTML markup

- Bạn có thể remove event listeners sử dụng phương thức `removeEventListener()`

![](https://i.imgur.com/v3jdRJC.png)

- Parameter event là loại event (click, mouseover)
- Parameter function là hàm chúng ta sẽ gọi khi mà event xảy ra
- useCapture là giá trị boolean chỉ định liệu sử dụng event bubbling hay event capturing (Optional)

**Note**: Bạn không sử dụng "on" prefix cho event, sử dụng `click`  thay vì `onclick` 

#### Add an Event Handler to an Element
- 






