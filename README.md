# jquery-progress [![spm version](http://spmjs.io/badge/jquery-progress)](http://spmjs.io/package/jquery-progress)

AUTHOR WEBSITE: [http://ydr.me/](http://ydr.me/)

jquery.fn.progress canvas 进度条

**五星提示：当前脚本未作优化、未完工，请勿用在生产环境**

__IT IS [A SPM PACKAGE](http://spmjs.io/package/jquery-progress).__




#USAGE
```
var $ = require('jquery');
require('jquery-progress')($);


// 1、初始化
$().progress({...});

// 2、设置进度
会暂停运动
$().progress(.5);

// 3、操作控制
// 暂停
$().progress("pause");
// 继续
$().progress("continue");
// 运行
$().progress("run",0,1,6000);

```



#OPTIONS
```
$.fn.progress.defaults = {
    // 是否逆时针递增
    // flase：顺时针递增，逆时针递减
    // true：逆时针递增，顺时针递减
    anticlockwiseAsc: false,
    // 开始角度，以水平向右方向为0度，顺时针+，逆时针-
    // 默认-90度为垂直向上方向
    beginAngle: -90,
    // 进度步进，为小于1的数
    step: 0.01,
    // 初始的进度
    progress: 0,
    // 运动进度的开始进度
    begin: 0,
    // 运动进度的结束进度
    // 如果开始进度大于结束进度，则进度递减，否则递增
    end: 1,
    // 运动进度的进度时间
    duration: 6000,
    // 背景类型：arc（圆弧），sector（扇形）
    bgType: "arc",
    // 前景类型：arc（圆弧），sector（扇形）
    fgType: "arc",
    // 背景样式
    bgStyle: {
        // 线头：butt，round 和 square
        lineCap: "butt",
        // 线宽
        lineWidth: 1,
        // 轮廓颜色
        strokeStyle: "#ccc",
        // 填充颜色
        fillStyle: "#ccc"
    },
    // 前景样式
    fgStyle: {
        // 线头：butt，round 和 square
        lineCap: "butt",
        // 线宽
        lineWidth: 1,
        // 轮廓颜色
        strokeStyle: "#0595FC",
        // 填充颜色
        fillStyle: "#0595FC"
    },
    // 进度开始回调
    onstart: $.noop,
    // 进度暂停回调
    onpause: $.noop,
    // 进度继续回调
    oncontinue: $.noop,
    // 进度结束回调
    onstop: $.noop,
    // 进度回调
    onprogress: $.noop
};
```
