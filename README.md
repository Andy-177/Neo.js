# Neo.js

## 一个基于前端的JS运行工具

### JavaScript 控制台工具教程

1. 项目文件准备
项目文件是一个包含多个文件的 ZIP 文件，通常包括以下内容：
- JavaScript 文件：你的代码文件，文件名以 `.js` 结尾。
- lib.cfg 文件：一个文本文件，列出需要下载的库文件的 URL，每行一个。

示例项目文件结构

```
project.zip
├── main.js
├── lib.cfg
└── other.js
```

示例 lib.cfg 文件内容

```
https://example.com/lib1.js
https://example.com/lib2.js
```

2. 控制台命令
以下是控制台支持的命令及其用途：

2.1 load
用途：加载一个项目文件（ZIP格式）。
操作：在控制台输入 `load`，然后选择一个项目文件。如果项目文件中包含 `lib.cfg` 文件，会自动下载其中指定的库文件。

2.2 list
用途：列出当前项目中的所有文件。
操作：在控制台输入 `list`，查看当前加载的项目中的文件列表。

2.3 js 
用途：运行指定的 JavaScript 文件。
操作：在控制台输入 `js <filename>`，其中 `<filename>` 是你想要运行的文件名，文件名必须以 `.js` 结尾。

2.4 unload
用途：卸载当前项目。
操作：在控制台输入 `unload`，清除当前加载的项目文件和下载的库文件。

2.5 lib
用途：导出当前项目中下载的库文件。
操作：在控制台输入 `lib`，将下载的库文件打包为一个 ZIP 文件，文件名为项目名加 `-lib.zip`。

2.6 redown
用途：重新下载 `lib.cfg` 文件中指定的库文件。
操作：在控制台输入 `redown`，重新下载 `lib.cfg` 文件中指定的库文件。

2.7 dlist
用途：列出当前正在下载的文件及其状态。
操作：在控制台输入 `dlist`，查看当前正在下载的文件及其状态。

2.8 dstop
用途：终止所有正在进行的下载操作。
操作：在控制台输入 `dstop`，终止所有正在进行的下载操作。

2.9 clear
用途：清除控制台屏幕。
操作：在控制台输入 `clear`，清除屏幕上的所有输出。

2.10 run
用途：直接打开并运行一个 JavaScript 文件，不需要依赖于项目。
操作：在控制台输入 `run`，然后选择一个 `.js` 文件，该文件将被直接运行。

3. 示例操作
假设你已经准备了一个名为 `project.zip` 的项目文件，其中包含 `main.js` 和 `lib.cfg` 文件。

1. 加载项目

```
> load
项目加载成功
库 https://example.com/lib1.js 下载成功
库 https://example.com/lib2.js 下载成功
```

2. 列出项目文件

```
> list
当前项目中的文件:
main.js
lib.cfg
other.js
```

3. 运行 JavaScript 文件

```
> js main.js
文件 main.js 运行成功
```

4. 导出库文件

```
> lib
库已导出为 project-lib.zip
```

5. 重新下载库文件

```
> redown
库 https://example.com/lib1.js 下载成功
库 https://example.com/lib2.js 下载成功
```

6. 列出正在下载的文件

```
> dlist
正在下载的文件:
https://example.com/lib1.js - 状态: completed
https://example.com/lib2.js - 状态: completed
```

7. 终止所有下载

```
> dstop
所有文件的下载已终止
```

8. 清除屏幕

```
> clear
屏幕已清除
```

9. 卸载项目

```
> unload
项目已卸载
```

10. 直接运行一个 JavaScript 文件

```
> run
选择一个 .js 文件后，文件将被直接运行
```

通过这些简单的命令和操作，你可以方便地管理和运行你的项目文件和库文件。希望这个教程对你有帮助！
