# 恶魔轮盘赌模组加载器
**This readme page is also avaliable in [English](README.md)!**

**适用于 Windows 和 Linux 平台的完整多人游戏支持, 包含 STEAM 上的 2.1.0.11 和 ITCH 上的 1.2.2.3!**\
适用于恶魔轮盘赌的模组加载器, 基于  [godot-mod-loader](https://github.com/GodotModding/godot-mod-loader) 的 4.x 分支.\
\
![BRML 主界面](img_docs/BRMLMainScreen.png "BRML 主界面")
![BRML 模组菜单](img_docs/BRMLModMenu.png "BRML 模组菜单")
## 信息
此仓库不包含由 Mike Klubnika 制作的恶魔轮盘赌的游戏源代码. 但包含一个 .xdelta 格式的修补文件 (和一个 .exe 格式的安装程序) 来修补原始游戏的最新版本. (Steam 上的 v2.1.0.11 和 itch.io 上的 v1.2.2.3) [可在 Steam 上购买](https://store.steampowered.com/app/2835570), [也可在 itch.io 上购买](https://mikeklubnika.itch.io/buckshot-roulette).

**我们不为盗版的游戏提供任何支持.**
Mike Klubnika 和 Critical Reflex 在这个游戏上花了不少功夫. 请尊重对待他们并抵制盗版行为. 任何没有所有权的请求查看源代码的请求都会被忽略.

## 可用的一些模组
_此列表已经因为最新更新而过期了, 我们很快就会更新它!_
- 由 AGO061 制作的 [测试模组](mods/TestMod_ZH.md) ([支持的模组加载器版本](mods/ModLoaderVersionSupport_ZH.md#testmod-by-ago061)) - 一个基础的可以将肥皂从水池的一边移动到另一边的测试模组.
- 由 AGO061 制作的 [OpenGL3 修复](mods/OpenGL3Fix_ZH.md) ([支持的模组加载器版本](mods/ModLoaderVersionSupport_ZH.md#opengl3-fix-by-ago061)) - 一个修复了 OpenGL3 渲染器的一些突出问题的模组. 此模组需要在游戏执行参数后添加 `-cm` 才能工作. 在 Windows 上创建一个快捷方式并将 `--rendering-driver opengl3 -cm` 添加到可执行文件路径末尾即可更轻松的使用 OpenGL3 渲染器 + 一些修复来运行游戏.
- 由 ITR 制作的 [更聪明的庄家](https://github.com/ITR13/BuckshotRouletteSmarterDealer/releases/latest) ([支持的模组加载器版本](mods/ModLoaderVersionSupport_ZH.md#smarter-dealer-by-itr)) - 一个绝对会想尽办法把你撕碎的庄家.
- 由 EmK530 制作的 [原生分辨率](https://github.com/EmK530/BRMods/tree/BRML/NativeResolution/Release) ([支持的模组加载器版本](mods/ModLoaderVersionSupport_ZH.md#native-resolution-by-emk530)) - 一个可以将游戏分辨率提升到匹配你的显示器的模组.
- 由 StarPandaBeg 制作的 [挑战包](https://github.com/StarPandaBeg/ChallengePack) ([支持的模组加载器版本](mods/ModLoaderVersionSupport_ZH.md#challenge-pack-by-starpandabeg)) - 一个可以隐藏子弹和物品的模组, 带有配置菜单.
- 由 ScientificGuy 制作的 [庄家的脸](https://github.com/ScientificGuy/BuckshotRouletteMods/releases/latest) ([支持的模组加载器版本](mods/ModLoaderVersionSupport_ZH.md#dealer-face-by-scientificguy)) - 每局结束后自动重置庄家的脸.
- 由 ScientificGuy 制作的 [错误修复](https://github.com/ScientificGuy/BuckshotRouletteMods/releases/latest) ([支持的模组加载器版本](mods/ModLoaderVersionSupport_ZH.md#bug-fixes-by-scientificguy)) - 修复了诸如重置时的慢动作的错误.

防止我在此忘记列出部分模组, 请查看[这个](mods/ModLoaderVersionSupport_ZH.md)文件. 
## 目前支持的功能
- 基础模组支持: 允许加载与游戏文件夹在同一目录的 mods 文件夹内的自定义模组 zip.
- 常规修复: 修复了使用 [GDRE Tools](https://github.com/bruvzg/gdsdecomp) 反编译后的游戏的部分错误.
- 默认渲染引擎: 此版本仍然默认使用 Forward+ 渲染器 (不像那些绝对不正规的网页版和手机版移植)
- 可以为你的 mod 添加自定义设置界面! (由于我没有多少时间去补充 wiki, 所以请查看[测试模组](mods/TestMod_ZH.md)的源代码来了解如何添加你的自定义设置界面)
- 在你自己的[服务器](#服务器)上开设多人游戏服务. **警告:** 修补后的游戏不支持 STEAM 的在线多人联机!

## 优势
- 更容易安装模组
- 可以在游戏的反编译版本的基础上制作模组，然后直接在模组加载器上使用，或者你可以尝试反编译修补后的游戏并从那里开始制作。

## 已知问题
- 缺少对游戏版本、模组依赖和冲突的检查.
- 不支持 Steam 成就 / 多人游戏 (道德原因, 无需过多讨论)

# 安装
## Windows
### 所需文件
- Buckshot Roulette.exe (Steam 上的 v2.1.0.11 或 itch.io 上的 v1.2.2.3)
- BRML_setup.exe ([可点击此处或右侧的 "Releases" 选项获取](https://github.com/AGO061/BuckshotRouletteModLoader/releases/latest))
  _或_
- 一个增量修补软件 (不推荐)

在安装完原版游戏后运行 .exe 安装程序. 安装程序便会自动将其安装到 `文档` 文件夹. 然后自行创建快捷方式、使用内置的 `brml.bat` 文件或直接打开修改后的 .exe 文件来运行游戏. 就是这么简单!

## Linux
### 所需文件
 - Buckshot Roulette.x86_64 (Steam 上的 v2.1.0.11 或 itch.io 上的 v1.2.2.3)
 - xdelta3 (`sudo apt install xdelta3`)
 - unzip (`sudo apt install unzip`)

当 `Buckshot Roulette.x86_64` 在你电脑上的任意一个文件夹内后, 运行以下命令并输入你实际的游戏文件路径:
```
mkdir Buckshot\ Roulette
cd Buckshot\ Roulette
mkdir mods override configs
wget https://github.com/AGO061/BuckshotRouletteModLoader/releases/download/3.1.0/brml3_linux_steam.xdelta
wget https://github.com/AGO061/BuckshotRouletteModLoader/releases/download/3.1.0/brml.sh
xdelta3 -d -s ../Buckshot\ Roulette.x86_64 brml3_linux_steam.xdelta Buckshot\ Roulette.x86_64
rm brml3_linux_steam.xdelta
chmod +x brml.sh Buckshot\ Roulette.x86_64
```
*标注: 如果需要则将 `brml3_linux_steam.xdelta` 替换为 `brml3_linux_itch.xdelta`.*

完成后你可以在 `Buckshot Roulette` 文件夹内使用命令 `./brml.sh` 启动游戏.

## 服务器
### 所需文件
 - brml3_server.exe (Windows)
   _或_
 - brml3_server.x86_64 (Linux)

运行服务器可执行文件, 即可在原生多人游戏中 (也就是为加任何模组的版本) 与其他玩家联机. 你​​可以在模组配置菜单中为模组加载器 (模组 -> 齿轮图标) 指定服务器 URL 并设置用户名. 

为了让其他网络的玩家和你一起游玩:
 - 找到开设服务器的设备的 IP 地址
 - 在你的路由器设置内将 UDP 协议的 2096 端口转发出去
 - 找到你的公网 IP 地址 (在网上搜索 "我的 IP 地址是多少" 或查看你的路由器设置) 然后将 IP 地址告诉其他玩家

## 排错
若想使用 OpenGL3 渲染器运行 Windows 版, 找到 `brml.bat` 内的此行内容:
```
start "" "%%i"
```
  然后修改为:
```
start "" "%%i" --rendering-driver opengl3
```
而 Linux 的 `brml.sh` 文件, 则需找到此行内容:
```
$game
```
  然后修改为:
```
$game --rendering-driver opengl3
```
可将任何安装时遇到的问题提交到 Issues 页面 (不会英文可使用[翻译器](https://fanyi.baidu.com)).

# 安装模组
如果你使用了上述的安装方式, 那么游戏文件夹内应该已经有一个 `mods` 文件夹了. 否则, 在游戏根目录自行创建一个 `mods` 文件夹即可. 然后将所有的模组 zip 放到文件夹内. 可查看此仓库的 `mods` 文件夹来试试一个将厕所里的肥皂移动了的测试模组.

# 开发
请查看 [BRML 开发 wiki](https://github.com/AGO061/BuckshotRouletteModLoader/wiki) 了解更多
