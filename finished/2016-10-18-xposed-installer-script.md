---
title: 【作死系列】你如何安装 Xposed 框架？
category: blog
permalink: /p/259184
layout: post
description: 不准用 custom recovery，不准用 flashfire 和 flashify。

---

作死给我锤升级了 SOS 2.6.8。。。发热严重，电充不满，果断回滚。回到 2.6.2 就可以安装 Xposed 模块了。

想想还有点小激动呢 WAW

先是求助于万能的 GitHub 找到了一个安装用的installer.bin，结果完全不能用啊qaq，老是报找不到目录，尼玛，还把我存储卡说是一个文件，真是服了

后来找到的是这个东西：

<http://androidforums.com/threads/guide-installing-xposed-without-flashfire.1071558/>

给了一个 installer.bin

看着不错，只是安装器是法语的。。。我就日了狗了

安装步骤如下：

- 下载对应版本的 Xposed 官方卡刷包。安装器上给出的说明是：

- ```
  Recuerda que:
   
   SDK 21 --> Android 5.0
   SDK 22 --> Android 5.1
   SDK 23 --> Android 6.0
  ```

- 这个不用翻译的吧。。。

- 然后如果文件正确的话，这里就会报出来：

- ``` 
  Estas instalando Xposed v86 para SDK 22
  Si no es el correcto no llegara a instalarse
  ```

- 大概就是说检测到的版本是 SDK 22，如果不是正确的版本就不要装（？）。我是 5.1 的桌子机=_=

- 然后……

- ```
  Presiona 1 para continuar:
  ```

- 按 1 键继续。。。

- ```
  Busybox instalado correctamente en Xbin.
  -El SDK de Xposed es el correcto (22).
  -La arquitectura del procesador es de 64 Bits
  Al igual que el Xposed que intenta instalar.
  ```

- 。。。这是啥。。。管它的反正是绿色，应该是没错的。。。

- ```
  Montando particiones...
  Creando directorios...
  Descomprimiendo archivos...
  ```

- 嗯这个我懂，

- ```
  Archive:  /sdcard/xposed-v86-sdk22-arm64.zip
    inflating: META-INF/com/google/android/flash-script.sh
    inflating: META-INF/com/google/android/update-binary
    inflating: META-INF/com/google/android/updater-script
    inflating: system/bin/app_process32_xposed
    inflating: system/bin/app_process64_xposed
    inflating: system/bin/dex2oat
    inflating: system/bin/oatdump
    inflating: system/bin/patchoat
    inflating: system/framework/XposedBridge.jar
    inflating: system/lib/libart-compiler.so
    inflating: system/lib/libart.so
    inflating: system/lib/libsigchain.so
    inflating: system/lib/libxposed_art.so
    inflating: system/lib64/libart-disassembler.so
    inflating: system/lib64/libart.so
    inflating: system/lib64/libsigchain.so
    inflating: system/lib64/libxposed_art.so
    inflating: system/xposed.prop
    inflating: META-INF/MANIFEST.MF
    inflating: META-INF/CERT.SF
    inflating: META-INF/CERT.RSA
  ```

- 终于有英文了qaq。。。

- ```
  Comprobando Xposed...
  Moviendo archivos...

  Fin de la instalacion

  Ahora ve a Xposed y haz un reinicio suave
  Al iniciar el sistema estara optimizando apps
  Dependiendo de las aplicaciones instaladas,
  tardara segundos hasta una hora.
  Si todo esta bien, Xposed estara activo.

  Se ha creado un Log de la instalacion
  en la ruta /sdcard

  Saludos!

  ```

- 不懂。。。但是我看见了 Saludos。。。想起了salute。。。好像装完了qaq

那，重启。。。

优化应用。。。(⊙ˍ⊙)

完了qaq

(～o￣▽￣)～o 。。。滚来滚去……o～(＿△＿o～) ~。。。

安装脚本给你们供玩坏：

[下载](https://o0stweauh.qnssl.com/installer.bin)

麻麻再也不担心我装不上 Xposed 辣