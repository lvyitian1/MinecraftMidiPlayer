# Minecraft Midi Player
a simple plugin to play midi in your minecraft server!   
Minecraft version: 1.8.1+   
# How to use  
0. Download the Latest version of this plugin from [releases](https://github.com/khjxiaogu/MinecraftMidiPlayer/releases)   
1. Install this plugin in your minecraft server's plugins folder(Server Directory/plugins/).   
2. Start server, wait before fully loaded and generates a folder named "MCMIDI".   
3. Place your midi music files inside MCMIDI folder.   
4. Use`/mcmidi load foo.mid`to load foo.mid into memory before first play.    
5. After loading,you can use`/mcmidi play foo.mid player`to play midi for a player or`/mcmidi play foo.mid` to play for yourself.   
6. If you wants to generate note block structure, use `/mcmidi generate foo.mid` to generate a note block structure right at your location.  
# Regards
- Server tps may affect play speed.
- Midi files that are too fast may have some notes lost, the smallest time unit is a minecraft tick(50ms), notes closer than this may be considered as notes at the same moment.  
- The velocity,pressure or volume of a single key would not be considered as there's no way to present this in minecraft.  
- Only midi speed change message and key press messages would take effect.  
- generating structure may cause performance issues. There's no undo, so be careful!
- structure width must larger than 10, you can calculate a approxmate value by lengthInTicks*3(cell width)/250(height).
# Minecraft midi播放器   
适用于minecraft服务器的midi插件   
Minecraft版本：1.8.1+   
# 用法  
0. 在[Releases](https://github.com/khjxiaogu/MinecraftMidiPlayer/releases)下载本插件的最新版本。   
1. 把本插件放在插件文件夹(服务器目录/plugins/)。    
2. 启动服务器，等待完全开启并生成MCMIDI文件夹。  
3. 把midi音乐放在插件文件夹下MCMIDI文件夹内（服务器目录/plugins/MCMIDI）。  
4. 首次播放某个音乐时，需要使用`/mcmidi load 测试.mid`加载"测试.mid"到服务器缓存。  
5. 载入后，就可以使用`/mcmidi play 测试.mid 玩家`为玩家播放"测试.mid"，或者`/mcmidi play 测试.mid`为自己播放了。  
6. 也可以使用`/mcmidi generate 测试.mid`在你所在位置生成一个红石音乐结构。  
# 注意事项
- 服务器tps会影响播放速度。  
- 过快的midi文件可能会出现音符丢失，最小时间单位是1 mc tick(50ms)，间隔低于这个的音符会被认为是同一时间内的音符。
- 速度、压力和音量属性都不会被使用，因为在minecraft内很难表达这些属性
- 只有midi速度变化和按键按下信息会生效
- 生成红石音乐会导致性能问题和卡服，不能撤销，请慎重操作！
- 结构宽度最低为16，可以近似计算长度为 tick长度*3(单元宽度)/250(高度)
