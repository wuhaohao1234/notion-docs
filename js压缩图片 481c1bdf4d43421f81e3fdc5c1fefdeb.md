# js压缩图片

# js压缩图片

使用npm进行图片压缩

在前端开发中，经常会遇到需要对图片进行压缩的情况，以提高页面加载速度并降低网络带宽压力。本文将介绍如何使用npm包来压缩图片。

## 安装

使用以下命令安装npm包：

```
npm install --save-dev imagemin

```

## 使用

1. 在项目中创建一个图片文件夹，将需要压缩的图片放入其中。
2. 创建一个js文件，在其中编写以下代码：

```
const imagemin = require('imagemin');
const imageminPngquant = require('imagemin-pngquant');
const imageminJpegtran = require('imagemin-jpegtran');

imagemin(['img/*.{jpg,png}'], {
    destination: 'dist/images',
    plugins: [
        imageminJpegtran(),
        imageminPngquant({
            quality: [0.6, 0.8]
        })
    ]
}).then(() => {
    console.log('Images optimized');
});

```

1. 将上述代码中的`'img/*.{jpg,png}'`替换为需要压缩的图片所在文件夹的路径，将`'dist/images'`替换为压缩后的图片保存路径。
2. 在命令行中运行以下命令：

```
node yourFile.js

```

1. 压缩后的图片将保存在指定路径中。

## 结论

使用npm包进行图片压缩是一种简单而有效的方法，可以提高网站的性能和用户体验。在实际开发中，可以根据需要调整压缩比例和其他配置参数，以达到最佳的压缩效果。

在上述代码中，只压缩了`.jpg`和`.png`格式的图片。如果需要压缩矢量图像，可以使用`imagemin-svgo`插件。要使用该插件，可以在项目中安装`imagemin-svgo` npm包，然后将其添加到`plugins`数组中：

```
const imageminSvgo = require('imagemin-svgo');

plugins: [
    imageminSvgo({
        plugins: [
            {removeViewBox: false}
        ]
    })
]

```

上述代码中的配置将禁用`removeViewBox`插件，以避免破坏矢量图像的缩放行为。可以根据需要调整其他选项和插件，以达到最佳的压缩效果。