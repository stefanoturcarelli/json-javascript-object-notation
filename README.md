# JSON
JSON stands for JavaScript Object Notation. It is a text-based data format following JavaScript object syntax. Even though it closely resembles JavaScript object literal syntax, it can be used independently from JavaScript, and many programming environments feature the ability to read (parse) and generate JSON.

JSON exists as a string — useful when you want to transmit data across a network. It needs to be converted to a native JavaScript object when you want to access the data. This is not a big issue — JavaScript provides a global JSON object that has methods available for converting between the two.

```jsx
{
		"name": "John Doe",
		"age": 30,
		"address": {
			"street": "123 Main St",
			"city": "Anytown",
			"state": "Anystate",
			"zip": "12345"
		},
		"hobbies": ["reading", "gaming", "hiking"]
	}
```

## `JSON.stringify()`

`JSON.stringify()` converts a JavaScript object or value to a JSON string. 

 `JSON.stringify()` is a static method of the JSON object, so you don't need to create a new JSON object to use it.

When working with JSON data and `localStorage`, using `JSON.stringify()` is a common and efficient practice. Since `localStorage` can only store data as strings, converting your JSON data into a string representation with `JSON.stringify()` allows you to store and retrieve it quickly.

---

## `JSON.parse()`

`JSON.parse()` converts a JSON string to a JavaScript object or value.

 `JSON.parse()` is also a static method of the JSON object, so you don't need to create a new JSON object to use it.

When you use a class to create users, you can use `JSON.stringify()` to convert the user objects to JSON strings and store them in `localStorage`. When you retrieve the data from `localStorage`, you can use `JSON.parse()` to convert the JSON strings to user objects. However, JavaScript doesn't know that the objects are users, so you need to convert them to users. You can do this using the `Object.setPrototypeOf()` method.

We can use regular objects instead of classes to create the users when we do a game. This way, we don't need to use `Object.setPrototypeOf()` to convert the objects to users.

---
