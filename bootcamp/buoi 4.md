### Grid
-  Dùng để layout 2 chiều
- **Example**: https://www.w3schools.com/w3css/w3css_templates.asp

```css
.container {
	display: grid;
}
```

![](https://i.imgur.com/tprGeY5.png)


![](https://i.imgur.com/UplhThb.png)

- Note:
	- Grid area: Luôn luôn phải là hình chữ nhật


```css
*{
 margin: 0;
 padding: 0;
}

body {
	padding: 20px;
}

.item {
	background: orange;
	border: 1px solid grey;
	height: 50px;
}

.container {
	display: grid;
	grid-template-columns: 300px 200px;
}
```

```css
*{
 margin: 0;
 padding: 0;
}

body {
	padding: 20px;
}

.item {
	background: orange;
	border: 1px solid grey;
	height: 50px;
}

.container {
	display: grid;
	grid-template-columns: 400px 1fr 2fr;
	/* grid-template-columns: repeat(3,1fr) */
	grid-template-rows: 400px 200px 500px;
	/* grid-auto-rows: 60px; */
	/* grid-auto-rows: minmax(60px, auto) */
	grid-template-areas: 
	"header header header"
	"sidebar content content"
	"sidebar comment comment"
	"footer footer footer";

	column-gap: 10px;
	row-gap: 20px;
}
```

```css
.item-5 {
	/*
	grid-column-start: 2;
	grid-column-end: 4;

	grid-row-start: 2;
	grid-row-end: 4;
	*/
	grid-column: 2 / 4
	grid-row: 2 / 4
}
```

