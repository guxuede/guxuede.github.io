---
title: Auto Tiled 常见的几种BitMask
date: 2026-05-04 15:00:27
tags:
---

常见的瓦片方案  
![本地图片](Auto-Tiled-常见的几种BitMask/styles.PNG)  


# 先介绍Reduced方案(47 Piece 的子集:16 Piece Subset)  
![本地图片](Auto-Tiled-常见的几种BitMask/style1_0.PNG)
这种分格比较适用于方方正正的的地图(无转角).

### 首先是最简单的一种:
![本地图片](Auto-Tiled-常见的几种BitMask/style1.PNG)

下面3个tile 和中间的tile 是重复随机替换磁块.由于过于简单,不支持过渡,比如转角.
这个其实是Reduced的方案的更简化方案(reduced 已经是简化方案了),它只有reduced 的右上角部分.
![本地图片](Auto-Tiled-常见的几种BitMask/style1_1.PNG)


# 第二种:
![本地图片](Auto-Tiled-常见的几种BitMask/style4.PNG)

这个素材来自于RPGMaker,相较于第一种,多了块右上角(3,4,7,8),用来弥补不支持转角的不足  
(1,2,4,6 重复与9,12,21,24 用于RPGMaker 磁贴缩略图)  


下面实例素材来自与 LPC style.   
中间9块(粉红)是主体边缘,中间则是由  
右上角6块(粉红)重复随机替换磁块  
下面4块(粉红)则是内转角  
![本地图片](Auto-Tiled-常见的几种BitMask/style4_1.PNG)

使用效果:  
![本地图片](Auto-Tiled-常见的几种BitMask/style4_2.PNG)

这种磁贴,由于缺少某些衔接,所以某些拐点仍然有缺陷:  
![本地图片](Auto-Tiled-常见的几种BitMask/style4_3.PNG)

# 下面是最复杂的一种,也支持最全的(47-tile Autotile Full Bitmask, 又名Blob):
![本地图片](Auto-Tiled-常见的几种BitMask/style2.PNG)

支持过渡


下面是一种变体, 和上面类似(47-tile Autotile Full Bitmask):
![本地图片](Auto-Tiled-常见的几种BitMask/style3.PNG)


下面是一种简化变体:  
![本地图片](Auto-Tiled-常见的几种BitMask/style3_1.PNG)





# Wang Sets
A Blob tileset is a 47 tile subset of a 2-edge 2-corner Wang tileset.
Wang Sets contain 16 tiles, and are usually suited best for top-down artwork. Borders in the Wang Set are located in the middle of the tile, which allows for auto-tiling equivalent to that of the Blob Set with considerably less tiles.  
https://www.boristhebrave.com/permanent/24/06/cr31/stagecast/wang/blob.html


![本地图片](Auto-Tiled-常见的几种BitMask/style5.PNG)




TODO 收集更多组合


Godot Docs:
https://github.com/dandeliondino/godot-4-tileset-terrains-docs  

Assemble 3x3 bitmask to 47 tile Format  
https://github.com/HeartoLazor/autotile_generator  
https://github.com/pyrareae/GodotAutotileAssembler  

Bitmask Autotile Generator for Godot & Unity(Turn a single tile into a seamless 47-tile Autotile bitmask set with a live testing canvas.)  
https://jaconir.online/blogs/bitmask-autotile-guide  
https://jaconir.online/tools/bitmask-autotile-generator  

15-Tile Format(Wang) to 47 tile Format(Blob)  
https://github.com/itsjavi/autotiler  
https://route1rodent.itch.io/autotiler  


Web Autotyler is an autotile conversion tool for turning small/incomplete autotile tilesets into complete, fleshed-out ones.
It supports nine different input formats and three different output formats, and displays a preview.  
https://github.com/wareya/webtyler?tab=readme-ov-file  
https://wareya.github.io/webtyler/  



RPG Maker to Godot autotile converter  
https://github.com/jumpravs/autotile-converter



双瓦片系统  
https://github.com/pablogila/TileMapDual