It's a different way of writing strings.

Instead of using double or single quotation marks:

```javascript
'A String'
```

or

```javascript
"Another string"
```

you can use backticks (`)

```javascript
`Another way of writing strings`
```

Now why would we use that way of creating strings?

With that syntax, you can dynamically add data into a string like this:

```javascript
const name = "Max";
const age = 29;
console.log(`My name is ${name} and I am ${age} years old.`);
```

This is of course shorter and easier to read than the "old" way of concatenating strings:

```javascript
const name = "Max";
const age = 29;
console.log("My name is " + name + " and I am " + age + " years old.");
```
