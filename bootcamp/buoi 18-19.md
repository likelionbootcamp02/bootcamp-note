# Bootcamp - Buổi 17
## Javascript Fundamentals 2
### 1. Functions
- Function là một block code thực thi một tác vụ nào đó
- Hàm sẽ được thực thi khi được gọi (invoke/call)

```js
// Functions
function logger() {
	console.log('My name is Jonas');
}

// calling / running / invoking function
logger();
logger();
logger();
```

```js
function myFunction(p1, p2) {  
  return p1 * p2;   // The function returns the product of p1 and p2  
}
```

```js
function fruitProcessor(apples, oranges) {
const juice = `Juice with ${apples} apples and ${oranges} oranges.`;
	return juice;
}
const appleJuice = fruitProcessor(5, 0);
console.log(appleJuice);
const appleOrangeJuice = fruitProcessor(2, 4);
console.log(appleOrangeJuice);
```

- Tại sao phải sử dụng function?
	- Tái sử dụng code
	- Dễ bảo trì


Exercise:
```js
function myFunction() {
  alert("Hello World!");
}

// myFunction()
```


- Function Return
	- Khi js chạm tới return, thì hàm đó sẽ dừng thực thi và trả lại một giá trị nào đó

```js
function toCelsius(fahrenheit) {  
  return (5/9) * (fahrenheit-32);  
}


let x = toCelsius(77);  
let text = "The temperature is " + x + " Celsius";
```


### 2. Function Declarations vs. Expressions


```js
// Function declaration
function calcAge1(birthYear) {
	return 2022 - birthYear;
}
const age1 = calcAge(1997);


  
// Function expression
const calcAge2 = function (birthYear) {
	return 2022 - birthYear;
}

const age2 = calcAge2(1997);

console.log(age1, age2);
```


### 3. Arrow functions
```js
const calcAge3 = birthYear => 2022 - birthYear;
const age3 = calcAge3(1997);
console.log(age3);
```

### 4. Coding Challenge #1
- So sánh điểm GPA của 2 bạn (toán, lý, hoá)
- Bạn A có số điểm toán lý hoá lần lượt là: 70, 95, 80
- Bạn B có điểm toán lý hoá lần lượt là: 100, 65, 90
- Nếu bạn A cao hơn bạn B thì chúng ta sẽ thông báo là A win
- Nếu bạn A thấp hơn bạn B thì chúng ta sẽ thông báo là B win
- Nếu A và B bằng nhau thì chúng ta sẽ thông báo là A và B win
```js
const calcGPA = (toan, ly, hoa) => (toan + ly + hoa)/3
console.log(calcAverage(3, 4, 5));

const gpaA = calcGPA(97, 112, 80);
const gpaB = calcGPA(109, 95, 50);
console.log(gpaA, gpaB);

const checkWinner = (gpaA, gpaB) => {
	if (gpaA > gpaB) {
		console.log('A win 🏆');
	} else if (gpaB > gpaA) {
		console.log('B win 🏆');
	} else {
		console.log('A và B win');
	}
}


```
### 5. Array

```js
const friend1 = 'Michael';
const friend2 = 'Steven';
const friend3 = 'Peter';
```

Nếu bạn muốn tìm kiếm tên "Peter" thì bạn phải làm sao? Solution là tạo array kết hợp với vòng lặp!

- Array có thể giữ nhiều hơn một giá trị

```js
const friends = ['Michael', 'Steven', 'Peter'];
console.log(friends);
```


- Bạn có thể truy cập gía trị của array thông qua index
```js
const friends = ['Michael', 'Steven', 'Peter'];
friends[0]
```

- Cách để truy cập người cuối cùng trong array

```js
const friends = ['Michael', 'Steven', 'Peter'];
friends[friends.length - 1]
```

- Bạn có thể thay đổi gía trị của array thông qua index

```js
const friends = ['Michael', 'Steven', 'Peter'];
friends[0] = 'CR7'
```

- Cách khác để tạo ra một array
```js
const friends = new Array("Michael", "Steven", "Peter");
```

- Array có thể chứa nhiều kiểu dữ liệu khác nhau

```js
const firstName = 'Nguyen';
const friends = ['Michael', 'Steven', 'Peter'];
const jonas = [firstName, 'Huy', 1997, 'teacher', friends];
```

Exercise:
```js
const calcAge = function (birthYeah) {
	return 2022 - birthYear;
}

const years = [1990, 1967, 2002, 2010, 2018];
const age1 = calcAge(years[0]);
const age2 = calcAge(years[1]);
const age3 = calcAge(years[years.length - 1]);

console.log(age1, age2, age3);

const ages = [calcAge(years[0]), calcAge(years[1]), calcAge(years[years.length - 1])];
console.log(ages);
```





### 6. Basic Array Operations (Method)
```js
const friends = ['Michael', 'Steven', 'Peter'];

// Add elements
const newLength = friends.push('Jay');
console.log(friends);
console.log(newLength);

friends.unshift('John');
console.log(friends);


// Remove elements
friends.pop(); // Last
const popped = friends.pop();
console.log(popped);
console.log(friends);

friends.shift(); // First
console.log(friends);
console.log(friends.indexOf('Steven'));
console.log(friends.indexOf('Bob'));


// Check value exists in array
console.log(friends.includes('Steven'));
console.log(friends.includes('Bob'));

if (friends.includes('Steven')) {
console.log('You have a friend called Steven');
}
```





### 7. Coding Challenge #2

- Tips calculator
```js
const calcTip = function (bill) {
	return bill >= 50 && bill <= 300 ? bill * 0.15 : bill * 0.2;
}

// const calcTip = bill => bill >= 50 && bill <= 300 ? bill * 0.15 : bill * 0.2;
const bills = [125, 555, 44];
const tips = [calcTip(bills[0]), calcTip(bills[1]), calcTip(bills[2])];
const totals = [bills[0] + tips[0], bills[1] + tips[1], bills[2] + tips[2]];

console.log(bills, tips, totals);
```

### 8. Objects
```js
const meArray = [
	'Huy',
	'Nguyen',
	1997,
	'teacher',
	['Michael', 'Peter', 'Steven']
];

const me = {
	firstName: 'Huy',
	lastName: 'Nguyen',
	birthYear: 1997,
	job: 'teacher',
	friends: ['Michael', 'Peter', 'Steven']
};
```

Ví dụ thực tế, **car** là một **object**
- Car có **properties** là weight và color
- Car có **method** là start và stop

![](https://i.imgur.com/Y3DFsyu.png)

- Tất cả các car có cùng properties nhưng khác giá trị
- Tương tự với methods

Ví dụ khác:
![](https://i.imgur.com/ibJ4IkD.png)


### 9. Dot vs. Bracket Notation
```js
const me = {
	firstName: 'Huy',
	lastName: 'Nguyen',
	birthYear: 1997,
	job: 'teacher',
	friends: ['Michael', 'Peter', 'Steven']
};

// Access value (Dot Notation)
me.firstName
me.lastName
me.friends[0] // 'Michael'

// Access value (Bracket Notation)
me["birthYear"]
me["job"]
me["friends"][1]

const nameKey = 'Name';
console.log(me['first' + nameKey]);
console.log(me['last' + nameKey]);

// Add a pair of key and value
me.location = 'Viet Nam';
me['email'] = 'huynguyen@gmail.com';
```

### 10. Object Methods

```js
const me = {
	firstName: 'Huy',
	lastName: 'Nguyen',
	birthYear: 1997,
	job: 'teacher',
	friends: ['Michael', 'Peter', 'Steven'],
	calAge: function() {
		return 2022 - this.birthYear
	}

	hasLegal: function() {
		const age =  this.calAge()
		if (age >= 18) {
			return true;
		} else {
			return false;
		}
	}
};

```
- This là gì?
	- This trả về cho bạn một object tuỳ thuộc vào context (ngữ cảnh)

![](https://i.imgur.com/krkYutb.png)


### 11. Coding Challenge #3
- Tạo một object với variables là `me` 
- Với các thuộc tính (properties) là `fullName`, `weight`, `height`
- Với các phương thức (methods) là `calcBMI`

```js
const me = {
	fullName: 'Huy Nguyen',
	weight: 79,
	height: 179,
	calcBMI: function () {
		this.bmi = this.mass / (this.height /  100) ** 2;
		return this.bmi;
	}
};

const yours = {
	fullName: 'B Nguyen',
	weight: 70,
	height: 170,
	calcBMI: function () {
		this.bmi = this.mass / (this.height /  100) ** 2;
		return this.bmi;
	}
};

me.calcBMI();
yours.calcBMI();
```

### 12. Iteration: The for Loop

- Vấn đề:
```js
const friends = ['Michael', 'Peter', 'Steven'];
console.log("Hello, " + friends[0])
console.log("Hello, " + friends[1])
console.log("Hello, " + friends[2])
// ...
```

- Loop thực thi một block code với n lần

```js
for (let i = 0; i < 3; i++) {  
  console.log("Hello, " + friends[i])
}
```

- Giải thích:
	- **expression 1**: set variables i = 0 trước khi vòng lặp bắt đầu
	- **expression 2**: Định nghĩa điều kiện i <  3, nếu i >= 3 thì dừng vòng lặp
	- **expression 3**: Tăng i lên 1 đơn vị sau mỗi lần block code thực thi

```js
for (expression 1; expression 2; expression 3) {  
  // _code block to be executed_  
}
```
- Giải thích:
	- **expression 1**: Thực thi trước khi block code thực thi, và chỉ thực thi 1 lần duy nhất
	- **expression 2**: Định nghĩa điều kiện để thực thi block code (nếu ``true`` -> thực thi block code, còn ``false`` thì dừng thực thi block code)
	- **expression 3**: Thực thi sau mỗi block code, có thể thực thi nhiều lần

- Có một vài cách viết `for` loop
	- `for` : Lặp block code đó n lần
	- `for/in`: Lặp thông qua properties
	- `for/of`: Lặp thông qua methods


Exercise:
1. In ra giá trị từ 1 đến 9
2. In ra các giá trị trong fruits gồm `["Apple", "Banana", "Orange"]`


### 13. Breaking and Continuing
```js
const friends = ['Michael', 'Peter', 'Steven'];

// Find friend named Peter
for (let i = 0; i < friends.length, i++) {
	if (friends[i] === "Peter") {
		console.log("Peter Found!")
	} else {
		console.log("Not Found")
	}
}
```

- Breaking: Nhảy ra khỏi vòng lặp
```js
const friends = ['Michael', 'Peter', 'Steven'];

// Find friend named Peter
for (let i = 0; i < friends.length, i++) {
	if (friends[i] === "Peter") {
		console.log("Peter Found!")
		break;
	} else {
		console.log("Not Found")
	}
}
```

- Continuing: Nhảy ra khỏi 1 vòng của vòng lặp và tiếp tục vòng tiếp theo

### 14. Looping Backwards and Loops in Loops
- In ra số từ 9 -> 1
```js
for (let i = 9; i >= 1; i--) {
	console.log(i);
}
```

- Cho 2 array:
	- array 1: [1,2,3,4]
	- array 2: [1,2,3,4]

- Kết quả mong đợi:
	- 1 1
	- 1 2
	- 1 3
	- 1 4
	- 2 1
	- ....
	- 4 4

```js
for (let i = 0; i <= array1.length; i++) {
	for (let j = 0; j <= array1.length; j++) {
		console.log(i, j)
	}
}
```


### 15. The While Loop
- Loop sẽ thực thi khi điều kiện trả về giá trị `true`
```js
while (condition) {  
  // code block to be executed
}
```

```js
i = 1;
while (i < 10) {  
  console.log(i)
  i++;  
}
```

### 16. Coding challenge # 4
```js
const calcTip = function (bill) {
	return bill >= 50 && bill <= 300 ? bill * 0.15 : bill * 0.2;
}
const bills = [22, 295, 176, 440, 37, 105, 10, 1100, 86, 52];
const tips = [];
const totals = [];

for (let i = 0; i < bills.length; i++) {
	const tip = calcTip(bills[i]);
	tips.push(tip);
	totals.push(tip + bills[i]);
}

console.log(bills, tips, totals);
const calcAverage = function (arr) {
	let sum = 0;
	for (let i = 0; i < arr.length; i++) {
		// sum = sum + arr[i];
		sum += arr[i];
	}
	return sum / arr.length;
}

console.log(calcAverage([2, 3, 7]));
console.log(calcAverage(totals));
console.log(calcAverage(tips));
```