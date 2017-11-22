# HSKConfuse
# 阅读本篇文章，需要先会[class-dump.](http://www.jianshu.com/p/025fa775f3a6) O(∩_∩)O谢谢。
    iOS代码混淆
    最近三年一直待在银行做App,由于银行对安全要求较高，所以iOS的代码必须要有混淆的措施，初期实施了念茜姐的混淆方案，但是领导说，我们要自动混淆，方法名字不能一个一个的添加到func.list中，所以方法名只能从.m和.h文件中抽取了，但是如何屏蔽系统的方法名，暂行的策略是:将自己定义的方法名全部添加一个前缀。

    例如 “hsk_funtion1”； “hsk_funtion2”；“hsk_funtion3”；
    
   
   ![shell文件](http://upload-images.jianshu.io/upload_images/1485140-22eacdbae71ab997.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
   ![添加脚本的文件路径](http://upload-images.jianshu.io/upload_images/1485140-a55c20978ddbfbd9.png?imageMogr2/auto-orient/strip)
   
# 通过class-dump 反编译之后：Appdelegate 效果
![图片](http://upload-images.jianshu.io/upload_images/1485140-582bcb1447c76938.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
# 通过class-dump 反编译之后：ViewController 效果
![效果](http://upload-images.jianshu.io/upload_images/1485140-ba254eda8b20005e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
  
  [简书地址：http://www.jianshu.com/p/0d42e5c6361c](http://www.jianshu.com/p/0d42e5c6361c)
  ***
      如果在使用过程中遇到BUG，希望你能Issues我，谢谢
    
    
另送一份ios自动打包脚本，放在项目根目录下，傻瓜版
https://github.com/housenkui/autoComplie
