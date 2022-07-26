# Bootcamp - Buổi 2


### Kết hợp selector (Combine Selector)
- h2, h3 : Các selector có cùng styling


```css
h2 {
	font-size: 30px;
}

h3 {
	font-size: 25px;
}

h2, h3 {
	font-weight: 500;
	line-height: 1.2;
	text-transform: capitalize;
}
```

- div h1: Style các thẻ `h2` trong thẻ `div`

```css
div h2 {
	text-align: center;
}
```

Source: w3schools.com/cssref/css_selectors.asp



### Class và Id
- Giống: 
	-  khai báo tên cho các thẻ để có thể style hoặc là sử dụng tương tác trong DOM
- Khác:
	- Khi khai báo tên id cho thẻ nào đó thì sẽ ko dùng lại lần 2 nữa, còn class thì khai báo một lớp cho nhiều thẻ
	- Khai báo trong css thì id bắt đầu bằng `#`, class bắt đầu bằng `.`
	- Mục đích sử dụng khác nhau

```css
.heading {
	color: red;
} 

#heading-secondary {
	color: blue;
}
```

### Pseudo classes (Lớp giả)
- :first-child, :last-child
- nth-child(even)
- :not(:last-child)

```css
.text:first-child {
	text-align: center;
}

.text:last-child {
	text-align: center;
}

.text:nth-child(odd) {
	text-align: center;
}

.text:nth-child(even) {
	text-align: center;
}

.text:not(:last-child) {
	text-align: center;
}
```
