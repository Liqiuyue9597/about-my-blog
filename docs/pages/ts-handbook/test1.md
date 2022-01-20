# Hello TypeScript
## 安装TypeScript
使用npm或者yarn进行命令行形式安装，将TS进行全局安装:
```shell
npm install -g typescript
yarn add global typescript
```
全局安装成功后，就可以在全局使用`tsc`命令对TS代码进行编译。TS文件都以`.ts`结尾，比如`a.ts`，然后`tsc a.ts`将其编译为一个JS文件`a.js`。

## 编译代码
举个例子，我们定义一个hello.ts文件：
```typescript
const str:string = 'hello world!';
console.log(str);
```
然后在命令行执行`tsc hello.ts`，会在相同的文件夹位置得到一个同名的JS文件，里面的内容是:
```js
var str = "hello world!";
console.log(str);
```
会发现JS代码并没有对`str`变量进行`string`类型限制，这是因为 TypeScript 只会在**编译**时对类型进行静态检查，如果发现有错误，编译的时候就会报错。而在运行时，与普通的 JavaScript 文件一样，不会对类型进行检查。所以TS包在项目是属于devDependencies并不是dependencies，线上代码运行的都是TS转为JS之后的代码。

