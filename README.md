# Unity-Game-localization-tutorial-and-toolkit    
# Unity游戏汉化/本地化教程及工具包  
  
**字符集由MSK Ggroup-Icetric制作** 
  
**工具包内各工具来源：**  
AssetsBundleExtracto(UABE) https://github.com/DerPopo/UABE   
AssetStudio https://github.com/Perfare/AssetStudio   
Il2CppDumper https://github.com/Perfare/Il2CppDumper   
dnSpy https://github.com/0xd4d/dnSpy   
MetaDataStringEditor https://github.com/JeremieCHN/MetaDataStringEditor   
UnityL10nTool https://github.com/dmc31a42/UnityL10nTool   
FontMergeSupplementaryTools https://github.com/nowar-fonts/Warcraft-Font-Merger   
bmfont https://www.angelcode.com/products/bmfont/   
Notepad++ https://notepad-plus-plus.org/   
UnityEX https://forum.zoneofgames.ru/topic/36240-unityex/  
<<<<<<< Updated upstream
Unity3DExtractorOSE & UnityEXPluginOSE  http://blog.sina.com.cn/u/3027377595  
CS2CSV https://github.com/Helly0000/UnityTranz  
UABEA https://github.com/nesrak1/UABEA  
=======
Unity3DExtractorOSE & UnityEXPluginOSE  http://blog.sina.com.cn/u/3027377595
UnityTranz(CS2CSV) https://github.com/Helly0000/UnityTranz
UABEAvalonia https://github.com/nesrak1/UABEA
RemoveDuplicateText https://blog.csdn.net/zxfhahaha/article/details/80295653
>>>>>>> Stashed changes
  
**文字教程来源：**  
https://www.cnblogs.com/guobaoxu/p/12055930.html

**原创视频教程：**  
https://www.bilibili.com/video/BV12K4y1j7w7/  
  
**字符集说明Character set description：**  
First use the smaller number in that language,  
"n" is not recommended for priority use.  
  
*简体中文：*  
1 - GBK符号+通用规范汉字表(一级)  
2 - GBK符号+通用规范汉字表(二级)  
3 - GBK符号+通用规范汉字表(三级)  
4 - GBK  

*繁体中文：*  
1 - GBK符号+常用國字表  
3 - GBK符号+(次)常用國字表  
4 - GBK  
  
*韩语：*  
1 - KS1001  
  
*俄文/拉丁文/希腊文/日文(片假/平假)：*  
1 - GBK符号(该文件已针对性优化)  
  
*少数民族语言/多语言同时使用：*  
1 - GB18030(本字符集过于庞大，请谨慎使用)  
  
*不推荐优先使用：*  
1 - GB2312精简  
2 - GB2312  
2 - GB12345繁体  
  
***所有文件均包含【俄文/拉丁文/希腊文/日文(片假/平假)】，并已针对西班牙语Ññ优化。***  
***All files include [Russian / Latin / Greek / Japanese (Piece / Platform)] and are optimized for Spanish Ññ.***  
  
***字符越多，占用越大，所以应尽量选择更少的字符集。***  
***The more characters there are, the larger the footprint, so try to choose as few character sets as possible.***  

**Unity汉化流程**  
1、  
  若Mono后端使用dnSpy修改Assembly-CSharp.dll中的文字。  
  若il2cpp后端使用MetaDataStringEditor修改global-metada.dat中的文字。  
  使用UnityEX或UABE提取并修改游戏资源包内TextAsset文件中的文字(若有)。  
  
*运行游戏查看效果，如显示正常，则无需以下操作。*  
  
2、使用UnityL10nTool查看游戏中字体名称及格式。  
3、使用UnityEX提取并替换UnityDefaultFont(通常为*.ttf文件)。  
  
*若无TMP或NGUI字体，则无需以下操作。*  
  
4、  
  NGUI使用BMFont制作新字体。  
  TMP使用与游戏相进Unity3D引擎版本制作新字体。  
5、使用UnityEX查找被替换字体的Material、Texture2D、MonoBehavior三个文件的Path ID#。(前两种使用Search Name模式搜索，MonoBehavior需要使用Search Text模式搜索)  
6、在UABE中根据Path ID#查找到相应的三个文件，选择Dump-json方式导出。  
7、将制作好的新字体用【5、6】方式导出，并按教程内容修改json文件。  
8、将修改后的新字体json导入回资源包，保存。  
  
**运行游戏查看效果。**  
  
Unity localization process  
1.  
  If Mono backend uses dnSpy to modify the text in Assembly-CSharp.dll.  
  If the il2cpp backend uses MetaDataStringEditor to modify the text in global-metada.dat.  
  Use UnityEX or UABE to extract and modify the text (if any) in the TextAsset file in the game resource pack.  
  
*Run the game to see the effect. If the display is normal, the following operations are not required. *  
  
2. Use UnityL10nTool to view the font name and format in the game.  
3. Use UnityEX to extract and replace the UnityDefaultFont (usually a * .ttf file).  
  
*If there is no TMP or NGUI font, the following operations are not required. *  
  
4.  
  NGUI uses BMFont to make new fonts.  
  TMP uses the version of the Unity3D engine that goes with the game to make new fonts.  
5. Use UnityEX to find the Path ID # of Material, Texture2D, and MonoBehavior for the replaced font. (The first two types use Search Name mode to search, MonoBehavior needs to use Search Text mode to search)  
6. Find the corresponding three files according to Path ID # in UABE, and select Dump-json to export.  
7. Export the produced new font in [5, 6] mode, and modify the json file according to the contents of the tutorial.  
8. Import the modified new font json back to the resource package and save it.  
  
** Run the game to see the effect. **  
  
