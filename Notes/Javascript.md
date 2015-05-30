# Javascript Notes

### Reverse a String

```Javascript
function reverseString(str){
	return str;
};
reverseString('hello');
```

Use a variety of methods to split the string up into each letter, reverse the order of the letters, and finally put them back together:

```Javascript
function reverseString(str){
	return str.split('').reverse().join('');
}
reverseString('hello');
```

### Factorial algorithm
Create an algorithm that will return the factorial of any number given to it:

```Javascript
function factorialize(num){
	//insert algorithm here
	return num;
}
factorialize(5);
```

A factorial is when a number is multiplied by all numbers between 1 and that number. An example can be: `5!`

This means: `5 * 4 * 3 * 2 * 1`

Therefore we need to take the number given and subtract 1 from it each time before multiplying to the number given:

```Javascript
function factorialize(num){
	if(num===0){
	return 0;
	}if(num===1){
	return 1;
	}if(num>1){
	//algorithm goes here:
	return num * factorialize(num-1);
	}
	return num;
}
factorialize(5) //will return 120
```