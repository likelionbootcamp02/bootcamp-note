# Bootcamp - Buổi 16

## Javascript Fundamentals 1
### 1. Giới thiệu về Javascript
- HTML, CSS và JS là 3 ngôn ngữ mà các trình duyệt hiểu
- JS được tích hợp vào để cho trang web có tính tương tác hơn, còn gọi là trang web động
	- Thay đổi nội dung trong HTML
	- Thay đổi giá trị thuộc tính HTML
	- Thay đổi style HTML
	- Ẩn/hiện các phần tử HTML

### 2. Link Javascript file
- Inline
- Internal
- External

### 3. Variables

- Biến dùng để lưu trữ giá trị
	- Khai báo biến
	- Gán biến với giá trị nào đó

- Khai báo một biến

```js
var carName;
```

- Lúc này biến carName không có bất kì giá trị nào, nên giá trị nó sẽ là `undefined`
- Để gán cho chúng một giá trị thì chúng ta sẽ sử dụng `=`

```js
var carName;
carName = "Volvo";
```

- Hoặc là bạn có thể gán giá trị đến một biến khi bạn khai báo nó:
```js
var carName = "Volvo";
```

- Ví dụ:
```js
var x = 5;  
var y = 6;  
var z = x + y;
```

- Ở ví dụ trên:
	- x lưu trữ giá trị 5
	- y lưu trữ giá trị 6
	- z lưu trữ giá trị 11

- Các quy tắc đặt tên biến:
	- Tên biến có thể chứa chữ cái (letters), số (digits), `_` (underscore), và $ (dollar signs)
	- Tên biến phải bắt đầu với letter
	- Tến biến cũng có thể bắt đầu với `_` và `$`
	- Tên biến là một case sensetive
	- Tên biến không nên đặt trùng tên với javascript keyword

Exercise:
Create a variable called `name` and assign the value `Huy` to it.
```js
var name = "Huy";
```


### 4. Data types
- Biến có thể lưu trữ nhiều kiểu dữ liệu:
	- String
	- Number
	- Boolean
	- ....

- Data types là một concept cực kì quan trọng, vì mỗi data type sẽ có những hành vi (hành động) khác nhau

```js
10 + 20
"Hello" + "World"
```

```js
let x = 16 + "Volvo";

// Suy ra

let x = "16" + "Volvo";
```

Exercise:

```js
let x = 16 + 4 + "Volvo";

// 20Volvo
```


```js
let x = "Volvo" + 16 + 4;

// Volvo164
```

- Javascript types là dynamic
```js
var x = 5;       // x có kiểu dữ liệu là Number
x = "John";      // x có kiểu dữ liệu là String
```


- String:
	- Là một chuỗi các chữ cái hay ký tự  (`Hello world`)

```js
let carName1 = "Volvo XC60";   // Using double quotes  
let carName2 = 'Volvo XC60';   // Using single quotes
```

- Number:

```js
let x1 = 34.00;     // Written with decimals  
let x2 = 34;        // Written without decimals
```

- Boolean:
	- Boolean chỉ có 2 giá trị: `true` và `false`
	- Boolean thường được sử dụng trong trường hợp kiểm tra điều kiện

```js
let isActive = true;
let isOpen = false;
```

- Object
- Underfined
- Null


- Kiểm tra kiểu dữ liệu của một biến:

```js
typeof ""             // Returns "string"  
typeof "John"         // Returns "string"  
typeof 314            // Returns "number"
```


Exercise:
```js
let length = 16;          // Kiểu dữ liệu ?
let lastName = "Johnson"; // Kiểu dữ liệu ?
```


### 5. Var, let và const

- Có 3 cách khai báo (declare) một biến:
	- var
	- let
	- const

Không thể sử dụng một biến mà không khai báo
```js
var foo = 1;
console.log(foo);
bar = 2;
console.log(bar);
```



### 6. JavaScript Operators

- Các loại operators trong Javascript
	- Arithmetic Operators (Toán tử số học)
	- Assignment Operators (Toán tử gán)
	- String Operators (Toán tử cho chuỗi)
	- Comparison Operators (Toán tử so sánh)
	- Logical Operators (Toán tử logic)()

- Arithmetic Operators (Toán tử số học):
![](https://i.imgur.com/R1mS1Rz.png)

```js
let x = 5;  
let y = 2;  
let z = x + y;
let z = x * y;
```

- Assignment Operators (Toán tử gán)

![](https://i.imgur.com/DzoeucF.png)

```js
let x = 10;  
x += 5;
```


- String Operators (Toán tử cho chuỗi)
	- `+` được sử dụng để thêm chuỗi (concatenate)
	- `+=` cũng được sử dụng để thêm chuỗi

```js
let text1 = "John";  
let text2 = "Doe";  
let text3 = text1 + " " + text2;
```



- Comparison Operators (Toán tử so sánh)

![](https://i.imgur.com/QZ4gOyY.png)

```js
const myWeight = 80;
const yourWeight = 80;
const isEqual = myWeight == yourWeight

// true
```

- Logical Operators (Toán tử logic):

![](https://i.imgur.com/6GdqNJk.png)

```js
const gpa = 8.5;
const conduct = "Good"

const haveScholarship = (gpa >= 8.5) && (gpa === "Good")
// true
```


### 7. Operator precedence (Ưu tiên trong toán tử)
- Giống như toán học:
	- Nhân chia trước, cộng trừ sau
	- Trong ngoặc được thực thi trước

```js
console.log(3 + 10 * 2);   // logs 23
console.log(3 + (10 * 2)); // logs 23 because parentheses here are superfluous
console.log((3 + 10) * 2); // logs 26 because the parentheses change the order
```


### 8. Coding Challenge 1

- Cho chiều cao và cân nặng của 2 bạn học viên, so sánh chỉ số BMI của 2 bạn
```js
const myWeight = 95;
const myTall = 188;
const yourWeight = 85;
const yourTall = 176;
const myBMI = markWeight / markTall ** 2;
const yourBMI = johnWeight / johnTall ** 2;
const huyHigherBMI = huyBMI > yourBMI;
console.log(myBMI, yourBMI, huyHigherBMI);
```

### 9. Strings and Template Literals
- Template literals thay vì sử dụng quote ("") thì nó dùng dấu backtick để định nghĩa string:

```js
let text = `Hello World!`;
```

- Template string cũng cấp bạn một cách dễ dàng để truyền vào một biến hoặc là một expression trong chuỗi

```js
let firstName = "John";  
let lastName = "Doe";  
  
let text = `Welcome ${firstName}, ${lastName}!`;
```

```js
let price = 10;  
let VAT = 0.25;  
  
let total = `Total: ${(price * (1 + VAT)).toFixed(2)}`;
```

- Template string được giới thiệu trong ES6 (Javascript 2015)


### 10. If/else Statements

- Hay còn được gọi là conditional statements
- Được sử dụng để thực thi các hành động khác nhau phụ thuộc vào điều kiện khác nhau
	- Ví dụ: Nếu hôm nay mưa thì ở nhà, còn không thì mình sẽ đi xem phim
	- Điều kiện ở đây là trời có mưa hay không
		- Nếu có (true), thì hành động ở đây là ở nhà
		- Nếu không (false), thì hành động ở đây là xem phim


```js
const age = 14;
const isOldEnough = age >= 18;
if (isOldEnough) {
	console.log('Sarah can start driving license');
} else {
	const yearsLeft = 18 - age;
	console.log(`Sarah is too young. Wait another ${yearsLeft} years:)`);
}
```

```js
const birthYear = 2021;
let century;
if (birthYear <= 2000) {
	century = 20;
} else {
	century = 21;
}

console.log(century)
```


### 11. Coding Challenge 2

- Cho chiều cao và cân nặng của 2 bạn học viên, so sánh chỉ số BMI của 2 bạn sử dụng if/else statement
```js
const myWeight = 95;
const myTall = 188;
const yourWeight = 85;
const yourTall = 176;
const myBMI = markWeight / markTall ** 2;
const yourBMI = johnWeight / johnTall ** 2;
const huyHigherBMI = huyBMI > yourBMI;
console.log(myBMI, yourBMI, huyHigherBMI);
if (huyHigherBMI) {
	console.log(`My BMI (${myBMI}) is higher than yours (${yourBMI})!`);
} else {
	console.log(`Your BMI (${yourBMI}) is higher than mine! (${myBMI})`);
}
```



### 12. Type Conversion and Coercion (Chuyển đổi kiểu dữ liệu)

- Type Conversion
```js
const birthYear = "1997";
const legalYear = birthYear + 18;
```

```js
const birthYear = "1997";
const legalYear = Number(birthYear) + 18;
```

- Type Coercion
	- Tự động chuyển đổi kiểu dữ liệu từ kiểu này sang kiểu khác

```js
const birthYear = "1997";
const legalYear = birthYear + 18;
```

Exercise:
```js
console.log('I am '+ 23 + ' years old') // I am 23 years old
console.log('23' - '10' - 3);           // 10
console.log('23' + '10' + 3);           // 23103
console.log('23' * '2');                // 46
console.log('23' / '2');                // 11.5
```


### 13. Truthy and Falsy Values
-   JavaScript sử dụng Type conversion(chuyển đổi dữ liệu từ kiểu dữ liệu này sang kiểu dữ liệu khác) để ép giá trị bất kỳ thành một giá trị Boolean trong một ngữ cảnh yêu cầu giá trị Boolean.
-   Truthy và falsy là những giá trị mà JavaScript khi ép về kiểu Boolean, hoặc trong một ngữ cảnh Boolean, nó sẽ cho ra giá trị true hoặc false.

- Các giá trị falsy trong JS:

```js
if (false)
if (0)
if ("")
if (null)
if (undefined)
if (NaN)
```


```js
console.log(Boolean(0));
console.log(Boolean(undefined));
console.log(Boolean('Huy'));
console.log(Boolean({}));

console.log(Boolean(''));
```

```js
const money = 100;
if (money) {
	console.log("Don't spend it all ;)");
} else {
	console.log('You should get a job!');
}
```


### 14. Equality Operators: == vs. ===
```js
const age = '18';
if (age === 18) console.log('You just became an adult :D (strict)');
if (age == 18) console.log('You just became an adult :D (loose)');
```

- `=` là gán biến với một giá trị nào đó
- `==` toán tử so sánh, tuy nhiên nó sẽ biến đổi thành cùng kiểu dữ liệu trước khi so sánh
- `===` toán tử so sánh, tuy nhiên nó sẽ KHÔNG biến đổi kiểu dữ liệu trước khi so sánh

### 15. Coding challenge 3
- So sánh điểm GPA của 2 bạn (toán, lý, hoá)
- Bạn A có số điểm toán lý hoá lần lượt là: 70, 95, 80
- Bạn B có điểm toán lý hoá lần lượt là: 100, 65, 90
- Nếu bạn A cao hơn bạn B thì chúng ta sẽ thông báo là A win
- Nếu bạn A thấp hơn bạn B thì chúng ta sẽ thông báo là B win
- Nếu A và B bằng nhau thì chúng ta sẽ thông báo là A và B win

```js
const gpaA = (97 + 112 + 80) / 3;
const gpaB = (109 + 95 + 50) / 3;

if (gpaA > gpaB) {
	console.log('A win 🏆');
} else if (gpaB > gpaA) {
	console.log('B win 🏆');
} else {
	console.log('A và B win');
}
```


### 16. Switch statement
- Được sử dụng để thực thi các hành động khác nhau phụ thuộc vào điều kiện khác nhau (Giống với if/elsif/else)

```js
const day = 'friday';

switch (day) {
	case 'monday': // day === 'monday'
		console.log('Plan course structure');
		console.log('Go to coding meetup');
		break;

	case 'tuesday':
		console.log('Prepare theory videos');
		break;
		
	case 'wednesday':
	case 'thursday':
		console.log('Write code examples');
		break;

	case 'friday':
		console.log('Record videos');
		break;
		
	case 'saturday':
	case 'sunday':
		console.log('Enjoy the weekend :D');
		break;
	default:
		console.log('Not a valid day!');
}

if (day === 'monday') {
	console.log('Plan course structure');
	console.log('Go to coding meetup');
} else if (day === 'tuesday') {
	console.log('Prepare theory videos');
} else if (day === 'wednesday' || day === 'thursday') {
	console.log('Write code examples');
} else if (day === 'friday') {
	console.log('Record videos');
} else if (day === 'saturday' || day === 'sunday') {
	console.log('Enjoy the weekend :D');
} else {
	console.log('Not a valid day!');
}
```

```js
switch (new Date().getDay()) {  
  case 0:  
    day = "Sunday";  
    break;  
  case 1:  
    day = "Monday";  
    break;  
  case 2:  
     day = "Tuesday";  
    break;  
  case 3:  
    day = "Wednesday";  
    break;  
  case 4:  
    day = "Thursday";  
    break;  
  case 5:  
    day = "Friday";  
    break;  
  case 6:  
    day = "Saturday";
  default:
	day = "I dunno"
}
```


```js
switch (new Date().getDay()) {  
  case 4:  
  case 5:  
    text = "Soon it is Weekend";  
    break;  
  case 0:  
  case 6:  
    text = "It is Weekend";  
    break;  
  default:  
    text = "Looking forward to the Weekend";  
}
```





### 17. The Conditional (Ternary) Operator
```js

const drink = age >= 18 ? 'wine 🍷' : 'water 💧';
console.log(drink);


let drink2;
if (age >= 18) {
	drink2 = 'wine 🍷';
} else {
	drink2 = 'water 💧';
}
console.log(drink2);
console.log(`I like to drink ${age >= 18 ? 'wine 🍷' : 'water 💧'}`);
```


### 18. Coding challenge 4
- https://codepen.io/cphemm/pen/reNwWd

```js
const bill = 430;
const tip = bill <= 300 && bill >= 50 ? bill * 0.15 : bill * 0.2;
console.log(`The bill was ${bill}, the tip was ${tip}, and the total value ${bill + tip}`);
```

