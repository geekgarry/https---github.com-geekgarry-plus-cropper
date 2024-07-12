# plus-cropper

裁剪图片，传入图片地址，进行图片裁切，最后成功输出一个图片的 base64 数据,另外还可以旋转图片
添加滚轮缩放裁剪框，以及对图片旋转和缩放以及拖动，添加移动端触摸滑动，旋转图片和缩放图片等操作

## How to use it?

```
npm install plus-cropper
```

### How to use it in the project!

```
import PlusCropper from 'plus-cropper';

//第一种使用：使用show方法已经包含了初始化函数的作用
// 显示裁剪框，传入配置选项
PlusCropper.show({
    imageSrc: tempURL
    // ... 其他选项
});
// 设置裁剪回调函数
PlusCropper.onCrop((croppedImageDataURL) => {
    console.log("Plus裁剪后的图片数据：", croppedImageDataURL);
    // 可以在这里将裁剪后的图片数据上传到服务器或者进行其他操作
});
// 设置显示回调函数
PlusCropper.onShow(() => {
    console.log("Plus裁剪框已显示");
});
// 设置隐藏回调函数
PlusCropper.onHide(() => {
    console.log("Plus裁剪框已隐藏");
});

//第二种使用：当init和第二个show一起用时
//下面这两个方法使用时
PlusCropper.init({
    imageSrc: tempURL
    // ... 其他选项
});
PlusCropper.show();
...
//***************其他以上相同方法******************
...
```

### npm Docs

#### Documentation for the npm registry, website, and command-line interface

See [npm Docs](https://docs.npmjs.com/).
