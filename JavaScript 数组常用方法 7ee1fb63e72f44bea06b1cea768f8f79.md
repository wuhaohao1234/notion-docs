# JavaScript 数组常用方法

JavaScript 中的数组是一种特殊类型的对象，可以存储多个值。以下是 JavaScript 数组常用的方法：

## push()

向数组末尾添加一个或多个元素，并返回新数组的长度。

```
const arr = [1, 2, 3];
arr.push(4, 5);
console.log(arr); // [1, 2, 3, 4, 5]

```

## pop()

删除数组末尾的元素，并返回删除的元素。

```
const arr = [1, 2, 3];
const lastItem = arr.pop();
console.log(arr); // [1, 2]
console.log(lastItem); // 3

```

## shift()

删除数组开头的元素，并返回删除的元素。

```
const arr = [1, 2, 3];
const firstItem = arr.shift();
console.log(arr); // [2, 3]
console.log(firstItem); // 1

```

## unshift()

向数组开头添加一个或多个元素，并返回新数组的长度。

```
const arr = [1, 2, 3];
arr.unshift(4, 5);
console.log(arr); // [4, 5, 1, 2, 3]

```

## slice()

返回从指定位置开始到指定位置结束的元素，不会改变原数组。

```
const arr = [1, 2, 3, 4, 5];
const newArr = arr.slice(1, 4);
console.log(newArr); // [2, 3, 4]
console.log(arr); // [1, 2, 3, 4, 5]

```

## splice()

从指定位置开始删除指定数量的元素，并可选地插入新元素，会改变原数组。

```
const arr = [1, 2, 3, 4, 5];
arr.splice(2, 2, 'a', 'b');
console.log(arr); // [1, 2, 'a', 'b', 5]

```

## forEach()

对数组中的每个元素执行指定的函数。

```
const arr = [1, 2, 3];
arr.forEach(item => {
  console.log(item);
});
// 1
// 2
// 3

```

## map()

对数组中的每个元素执行指定的函数，并返回执行结果组成的新数组。

```
const arr = [1, 2, 3];
const newArr = arr.map(item => item * 2);
console.log(newArr); // [2, 4, 6]

```

## filter()

对数组中的每个元素执行指定的函数，返回执行结果为 `true` 的元素组成的新数组。

```
const arr = [1, 2, 3, 4, 5];
const newArr = arr.filter(item => item % 2 === 0);
console.log(newArr); // [2, 4]

```

## reduce()

对数组中的每个元素执行指定的函数，返回最终的计算结果。

```
const arr = [1, 2, 3, 4, 5];
const sum = arr.reduce((prev, curr) => prev + curr);
console.log(sum); // 15

```

以上是 JavaScript 数组常用的方法，还有很多其他的方法可以在需要的时候查阅文档。

# JavaScript 数组常用方法

JavaScript 中的数组是一种特殊类型的对象，可以存储多个值。以下是 JavaScript 数组常用的方法：

## push()

向数组末尾添加一个或多个元素，并返回新数组的长度。

```
const arr = [1, 2, 3];
arr.push(4, 5);
console.log(arr); // [1, 2, 3, 4, 5]

```

## pop()

删除数组末尾的元素，并返回删除的元素。

```
const arr = [1, 2, 3];
const lastItem = arr.pop();
console.log(arr); // [1, 2]
console.log(lastItem); // 3

```

## shift()

删除数组开头的元素，并返回删除的元素。

```
const arr = [1, 2, 3];
const firstItem = arr.shift();
console.log(arr); // [2, 3]
console.log(firstItem); // 1

```

## unshift()

向数组开头添加一个或多个元素，并返回新数组的长度。

```
const arr = [1, 2, 3];
arr.unshift(4, 5);
console.log(arr); // [4, 5, 1, 2, 3]

```

## slice()

返回从指定位置开始到指定位置结束的元素，不会改变原数组。

```
const arr = [1, 2, 3, 4, 5];
const newArr = arr.slice(1, 4);
console.log(newArr); // [2, 3, 4]
console.log(arr); // [1, 2, 3, 4, 5]

```

## splice()

从指定位置开始删除指定数量的元素，并可选地插入新元素，会改变原数组。

```
const arr = [1, 2, 3, 4, 5];
arr.splice(2, 2, 'a', 'b');
console.log(arr); // [1, 2, 'a', 'b', 5]

```

## forEach()

对数组中的每个元素执行指定的函数。

```
const arr = [1, 2, 3];
arr.forEach(item => {
  console.log(item);
});
// 1
// 2
// 3

```

## map()

对数组中的每个元素执行指定的函数，并返回执行结果组成的新数组。

```
const arr = [1, 2, 3];
const newArr = arr.map(item => item * 2);
console.log(newArr); // [2, 4, 6]

```

## filter()

对数组中的每个元素执行指定的函数，返回执行结果为 `true` 的元素组成的新数组。

```
const arr = [1, 2, 3, 4, 5];
const newArr = arr.filter(item => item % 2 === 0);
console.log(newArr); // [2, 4]

```

## reduce()

对数组中的每个元素执行指定的函数，返回最终的计算结果。

```
const arr = [1, 2, 3, 4, 5];
const sum = arr.reduce((prev, curr) => prev + curr);
console.log(sum); // 15

```

以上是 JavaScript 数组常用的方法，还有很多其他的方法可以在需要的时候查阅文档。