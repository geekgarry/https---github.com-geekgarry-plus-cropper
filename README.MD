# plus-cropper

裁剪图片，传入图片地址，进行图片裁切，最后成功输出一个图片的 base64 数据,另外还可以旋转图片

## How to use it?

```
npm install plus-cropper
```

### How to use it in the project!

```
import ImageCropper from 'plus-cropper';

const cropper = new ImageCropper({
    imageSrc: 'your image url', // 替换为你的图片地址
    auautoShow: false,//是否在初始化后显示裁剪，不写时默认为true，为false时，需要调用cropper.show();
});
cropper.onCrop((croppedImageDataURL) => {
    console.log('裁切后的图片数据(base64):', croppedImageDataURL);
    // 可以在这里将裁切后的图片数据上传到服务器或进行其他操作
});
cropper.onHide(() => {
    console.log("隐藏(取消)事件回调函数！");
});
cropper.onShow(() => {
    console.log("显示事件回调函数！");
});

cropper.show();//当autoShow: true时才需要使用，表示在初始化时不会自动显示裁剪框
```

### npm Docs
#### Documentation for the npm registry, website, and command-line interface

See [npm Docs](https://docs.npmjs.com/).