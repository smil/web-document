
## 前言

> `ECMAScript` 迄今为止标准定义了 `7` 种数据类型：`6` 种原始类型-- `String`、`Number`、 `Boolean`、 `Undefined`、`Null` 和 `Symbol`；`1` 种引用类型-- `Object`

看到这里，你是否已经对它们了如指掌呢。如果你还对它们之间的定义、转换、检测等方面并不是那么清楚，或者已经有些模糊。那么，下面就让我们一起去重新探索、温习一遍吧

如果文章中有出现纰漏、错误之处，还请看到的小伙伴多多指教，先行谢过

以下↓

### 原始值

> 除 `Object` 以外的所有类型都是不可变的（值本身无法被改变），我们称这些类型的值为 `原始值`

#### String 类型

> `JavaScript` 的字符串类型用于表示文本数据.`JavaScript` 字符串是不可更改的。这意味着字符串一旦被创建，就不能被修改。但是，可以基于对原始字符串的操作来创建新的字符串

```js
var a = 'hello'
```

#### Number 类型

> 根据 `ECMAScript` 标准，`JavaScript` 中只有一种数字类型：基于 `IEEE 754` 标准的双精度 `64` 位二进制格式的值（`-(263 -1)` 到 `263 -1`）

特殊的数值类型：

> 无穷大：`+Infinity()`，`-Infinity()` 和 `NaN` (非数值，`Not-a-Number`)

`NaN`，非数值。是一个特殊的 `Number` 类型，用来表示一个本来要返回数值的操作未返回数值的情况

- 任何涉及 `NaN` 的操作都返回 `NaN`
- `NaN` 与任何值都不相等，包括 `NaN` 本身

```js
40 / NaN  // NaN
NaN === NaN // false
```

> 最基本的数值字面量格式是十进制整数，还可以通过八进制或十六进制来表示。八进制字面值的第一位必须是 `0`，然后是八进制数字序列`（0 ~ 7）`。十六进制字面量的前两位必须是 `0x`，后跟任何十六进制数字`（0 ~ 9 以及 a ~ f）`。其中字母可以是大写也可以是小写

```js
var num1 = 070; // 八进制的56
var num1 = 079; // 无效的八进制，会解析为十进制的79
var num2 = 56; // 十进制的56
var num3 = 0x38; // 十六进制的56
```

#### Boolean 类型

> 表示一个逻辑实体，可以有两个值：`true` 和 `false`

```js
var suc = true;
var los = false;
```

#### Undefined 类型

> `Undefined` 类型只有一个值，即特殊的 `undefined` 。一个  声明但没有被赋值的变量会有个默认值 `undefined`

```js
var a;  // undefined
```

#### Null 类型

> `Null` 类型也只有一个值，即特殊的 `null` 表示一个空对象指针

```js
var foo = null;
```

#### Symbol 类型

> 符号 `(Symbols)` 是 `ECMAScript` 第 `6` 版新定义的。符号类型是唯一的并且是不可修改的

```js
var s = Symbol()
```
> `Symbol` 函数前不能使用 `new` 命令，否则会报错。这是因为生成的 `Symbol` 是一个原始类型的值，不是对象

> `Symbol` 函数可以接受一个字符串作为参数，表示对 `Symbol` 实例的描述






