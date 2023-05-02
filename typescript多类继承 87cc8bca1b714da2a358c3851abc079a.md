# typescript多类继承

# typescript 多类继承

在 TypeScript 中，我们可以使用 `extends` 关键字实现多类继承。多类继承是指一个类继承多个父类的特性。

下面是一个简单的例子：

```
class Animal {
  move() {
    console.log("Animal is moving");
  }
}

class Flyable {
  fly() {
    console.log("Flying...");
  }
}

class Bird extends Animal, Flyable {   // Error
  // ...
}

```

在上面的例子中，我们试图让 `Bird` 类同时继承 `Animal` 和 `Flyable` 类。但是 TypeScript 会报错，因为它不支持多类继承。

为了解决这个问题，我们可以使用接口来实现多类继承的效果：

```
interface Animal {
  move(): void;
}

interface Flyable {
  fly(): void;
}

class Bird implements Animal, Flyable {
  move() {
    console.log("Bird is moving");
  }

  fly() {
    console.log("Bird is flying");
  }
}

```

在上面的例子中，我们定义了两个接口 `Animal` 和 `Flyable`，它们分别定义了 `move()` 和 `fly()` 方法。然后我们让 `Bird` 类实现这两个接口，这样它就具有了 `Animal` 和 `Flyable` 两个类的特性。

总结一下，虽然 TypeScript 并不支持多类继承，但我们可以使用接口来实现类似的效果。