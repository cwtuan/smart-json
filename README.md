# Smart JSON - Prettify / Minify / Verify JSON Tool
Smart JSON is a superset of JSON and JSON5, which means that any valid JSON data is also valid Smart JSON data. However, Smart JSON allows for more flexible syntax, such as omitting quotes around property names and allowing for trailing commas in arrays and objects. This makes it easier to write and edit JSON.

![smart-json](https://user-images.githubusercontent.com/3455798/226092084-5977ae57-b643-473a-a0bd-b937084b07f7.gif)


## Comma
- Arrays may have a single trailing comma.
- Objects may have a single trailing comma.
- Missing comma in object is allowed.

```js
{
  "key1": [1, 2, ], // Trailing comma in array
  "key2": { "key1": "string", },  // Trailing comma in object 
  "key3": "string" // --> Missing comma in object is allowed
  "key4": "string"
}
```
![image](https://user-images.githubusercontent.com/3455798/226093599-ca5e8319-75fd-4c5d-861d-3ef0e0a53490.png)


## Comment
- Single comment(// or #) is allowed.
- Multi-line comment(/* */) is allowed.


```js
{
  // "key1": "string",

  /* "key2": "string",
     "key3": "string", */

  #  "key4": "string",
}
```
![image](https://user-images.githubusercontent.com/3455798/226093818-36c2cd20-0b35-4384-9ff1-7b3c3752ae40.png)


## String
- Strings may be single quoted.

```js
{
  singleQuotes: 'Use "double quotes"',
}
```
![image](https://user-images.githubusercontent.com/3455798/226093775-ce2e1a7c-cc47-43a9-9498-614e036c4492.png)



## Object key

- keys may be an ECMAScript 5.1 [IdentifierName](https://262.ecma-international.org/5.1/#sec-7.6).
- Object keys can be specified without quotes.
```js
{
  "$string": "string", // ECMAScript 5.1 IdentifierName
  unquoted: 'string' // Key without quotes
}
```
![image](https://user-images.githubusercontent.com/3455798/226093494-66983740-9a00-4041-bdc1-613732e89253.png)


## Number
- Numbers may be hexadecimal.
- Numbers may have a leading or trailing decimal point.
Numbers may be [IEEE 754](https://en.wikipedia.org/wiki/IEEE_754) positive infinity, negative infinity, and NaN.</li>
- Numbers may begin with an explicit plus sign.


```js
{
  "key1": 0xdecaf, // hexadecimal
  "key2": .8675309, // leading decimal point
  "key3": 8675309., // trailing decimal point
  "key4": +1, // positive sign
}
```
![image](https://user-images.githubusercontent.com/3455798/226093838-6323c3b6-bd20-4363-a2cb-bd210d3803a2.png)
