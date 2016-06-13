# 类型推论

> 如果没有明确的指定类型，那么 TypeScript 会依照类型推论的规则推断出一个类型。

## 什么是类型推论

以下代码虽然没有指定类型，但是会在编译的时候报错：

```ts
let myFavoriteNumber = 'seven';
myFavoriteNumber = 7;

// index.ts(2,1): error TS2322: Type 'number' is not assignable to type 'string'.
```

事实上，它等价于：

```ts
let myFavoriteNumber: string = 'seven';
myFavoriteNumber = 7;

// index.ts(2,1): error TS2322: Type 'number' is not assignable to type 'string'.
```

TypeScript 会在没有明确的指定类型的时候，这就是类型推论。

如果定义的时候没有赋值，则会推断成 `any` 类型：

```ts
let myFavoriteNumber;
myFavoriteNumber = 'seven';
myFavoriteNumber = 7;
```

## Links

- [Handbook - Type Inference](http://www.typescriptlang.org/docs/handbook/type-inference.html)
- [中文手册 - 类型推论](https://zhongsp.gitbooks.io/typescript-handbook/content/doc/handbook/Type%20Inference.html)