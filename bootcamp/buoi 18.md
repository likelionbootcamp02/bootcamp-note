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

