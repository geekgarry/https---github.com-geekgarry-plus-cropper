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

// 显示裁剪框，传入配置选项
PlusCropper.show({
    imageSrc: tempURL
    // ... 其他选项（可选）
    closableBtn: true,//默认通过右上角按钮关闭裁剪的界面
    cropAreaWidth: 150,//裁剪框初始长宽
    cropAreaHeight: 100,//裁剪框初始长宽
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
...
```

### npm Docs

#### Documentation for the npm registry, website, and command-line interface

See [npm Docs](https://docs.npmjs.com/).
