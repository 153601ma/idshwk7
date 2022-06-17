# idshwk7

####加密：
在win10下 命令行中使用命令 copy /b raw.jpg+name.jpg test.jpg  
此命令将两张图片以二进制形式拼接起来，结果图片看起来仍然是原图片。  


#### 解密
使用linux中的binwalk，运行binwalk test.jpg   

得到结果：

```

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             JPEG image data, JFIF standard 1.01  
x         y          JPEG image data, JFIF standard 1.01
```

由此在linux中在文件目录下使用命令 dd if=test.jpg of=ma.jpg skip=x bs=1 得到最终结果

