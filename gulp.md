### gulp的安装
首先确保你已经正确安装了node.js环境。然后以全局方式安装gulp:
```
npm install -g gulp
```
全局安装gulp后，还需要在每个要使用gulp的项目中都单独安装一次。把目录切换到你的项目文件夹中，然后
在命令行中执行:
```
npm install gulp
```
如果想在安装的时候把gulp写进项目package.json文件的依赖中，则可以加上--save-dev:
```
npm install --save-dev gulp
```
### 开始使用gulp
#### 建立gulpfile.js文件
gulp需要一个文件作为他的主文件，在gulp中这个文件叫做gulpfile.js。新建一个文件名为gulpfile.js的文件，
然后放到项目目录中。之后要做的事情就是在gulpfile.js文件中定义我们的任务了。  下面是一个最简单的gulpfile.js
文件内容示例，它定义了一个默认的任务。
```js
let gulp = require('gulp');
gulp.task('default', function(){
  console.log('Hello World...');
});
```

此时我们的目录结构是这样子的:
├── gulpfile.js
├── node_modules
│ └── gulp
└── package.json

要运行gulp任务，只需要切换到存放gulpfile.js文件的目录，然后在命令行中执行gulp命令就可以了。
gulp 后面可以加上要执行的任务名，例如 gulp task1，如果没有指定任务名，则会执行任务名为default的默认任务。

### gulp的API介绍
使用gulp，仅需要知道4个API即可:gulp.task(), gulp.src(), gulp.dest(), gulp.watch(), 所以很容易就能掌握，
但有几个地方需要理解透彻才行，为了避免出现理解偏差，建议先看一遍
