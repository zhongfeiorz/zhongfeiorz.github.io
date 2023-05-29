<a name="pKxZn"></a>
# user/setting.json
<a name="KiqLJ"></a>
## 简洁 配置
```json
{
  "editor.fontSize": 18,
  "editor.insertSpaces": true,  // 按tab 时插入空格
  "files.autoSave": "afterDelay", // 文件自动保存，使用 vim 插件，就不用每次保存了
  "editor.renderWhitespace": "all", //  4个空格显示为 .... 
  "editor.detectIndentation": false, //不要检测到第一个是tab，就后面都用tab，这样会覆盖默认设置。
  "editor.renderControlCharacters": true, // tab 显示为 -->
  "editor.cursorBlinking": "smooth",
  "editor.cursorSmoothCaretAnimation": "on",
  "cmake.generator": "MinGW Makefiles", // 要使用的 CMAKE 生成器

  // 启用vim 的情况下，使用 ctrl c 复制等能
  // 实现方法  关闭 vim 插件中，这些组合键的映射
  "vim.handleKeys": {
    "<C-a>": false,
    "<C-c>": false,
    "<C-x>": false,
    "<C-f>": false,
    "<C-h>": false,
    "<C-s>": false,
    "<C-z>": false,
    "<C-y>": false,
  },
  "vim.mouseSelectionGoesIntoVisualMode": false,
  "security.workspace.trust.untrustedFiles": "open",
  "remote.SSH.remotePlatform": {
    "zuocangbianyi": "linux"
  },
  "editor.unicodeHighlight.nonBasicASCII": false,
  "workbench.colorTheme": "One Dark Pro",

}
```
<a name="daOx1"></a>
## 丰富配置
```json
{
    "editor.fontSize": 18,
    "editor.insertSpaces": true,  // 按tab 时插入空格
    "files.autoSave": "afterDelay", // 文件自动保存，使用 vim 插件，就不用每次保存了
    "editor.renderWhitespace": "all", //  4个空格显示为 .... 
    "editor.detectIndentation": false, //不要检测到第一个是tab，就后面都用tab，这样会覆盖默认设置。
	"editor.renderControlCharacters": true, // tab 显示为 -->
	"cmake.generator": "MinGW Makefiles", // 要使用的 CMAKE 生成器

    "security.workspace.trust.untrustedFiles": "open",
    "remote.SSH.remotePlatform": {
        "zuocangbianyi": "linux"
    },
    "editor.unicodeHighlight.nonBasicASCII": false,
    "workbench.colorTheme": "One Dark Pro",
    "workbench.colorCustomizations": {
        // 光标的颜色设置
        "editorCursor.foreground": "#16C60C",
        // 当前行的背景颜色设置
        "editor.lineHighlightBackground": "#292e42",
        // 状态栏颜色设置
        "statusBar.background": "#1e1e1e",
        "statusBar.foreground": "#9b9b8f",
        "statusBar.border": "#333a48",
    },
    // 布局控制
    // "workbench.layoutControl.enabled": false,
    // 渲染行高的风格
    // "editor.renderLineHighlight": "line",
    // 取消 occurrence 和 selection 的高亮
    // "editor.occurrencesHighlight": false,
    // "editor.selectionHighlight": false,

    // vim settings
    // vim 是否使用系统剪贴板
    "vim.useSystemClipboard": false,
    // 开启 vim 的 easymotion
    "vim.easymotion": true,
    // 当输入一个搜索字符时，显示下一个匹配的结果
    "vim.incsearch": true,
    // vim 来接管 ctrl 键
    "vim.useCtrlKeys": true,
    // vim 打开高亮搜索
    // "vim.hlsearch": true,
    // 设置 vim 的 leader 键为空格键
    "vim.leader": "<space>",
    // vim 打开/关闭鼠标选择为 可视模式
    "vim.mouseSelectionGoesIntoVisualMode": false,
    // 光标的动画效果
    "editor.cursorBlinking": "smooth",
    "editor.cursorSmoothCaretAnimation": "on",

    // 启用vim 的情况下，使用 ctrl c 复制等能
	// 实现方法  关闭 vim 插件中，这些组合键的映射
    // 设置 vim 不接管某些快捷键
    "vim.handleKeys": {
        "<C-a>": false,
        "<C-c>": false,
        "<C-x>": false,
        "<C-f>": false,
        "<C-h>": false,
        "<C-s>": false,
        "<C-z>": false,
        "<C-y>": false,
    },

    // vim insert 模式下的键位设置
    "vim.insertModeKeyBindings": [
        {
          "before": ["j", "j"],
          "after": ["<Esc>"]
        }
      ],
    // vim normal 模式下的键位设置
    "vim.normalModeKeyBindings": [
        // 侧边栏的显示和隐藏的快捷键，我映射成了 leader + e
        {
        "before": [
            "leader",
            "e"
        ],
        "commands": [
            {
            "command": "workbench.action.toggleSidebarVisibility"
            }
        ]
        },
        // 在左侧的文件管理器中打开当前文件
        {
        "before": [
            "leader",
            "f"
        ],
        "commands": [
            {
            "command": "revealInExplorer"
            }
        ]
        },
        // 取消高亮，比如我们在当前文件中搜索之后可以使用这个快捷键
        {
        "before": [
            "leader",
            "h"
        ],
        "commands": [
            ":noh"
        ]
        },
        // 关闭当前的 tab
        {
        "before": [
            "leader",
            "q"
        ],
        "commands": [
            ":q"
        ]
        },
        // 保存当前的文件
        {
        "before": [
            "leader",
            "w"
        ],
        "commands": [
            ":w"
        ]
        },
        // 显示和隐藏左侧的活动栏
        {
        "before": [
            "leader",
            "a"
        ],
        "commands": [
            {
            "command": "workbench.action.toggleActivityBarVisibility"
            }
        ]
        },
        // 显示和隐藏底部的状态栏
        {
        "before": [
            "leader",
            "b"
        ],
        "commands": [
            {
            "command": "workbench.action.toggleStatusbarVisibility"
            }
        ]
        },
        // 快速在底部的 terminal 中运行 python 文件
        {
        "before": [
            "leader",
            "p",
            "y"
        ],
        "commands": [
            "workbench.action.files.saveAll",
            {
            "command": "workbench.action.terminal.sendSequence",
            "args": {
                "text": "clear \u000D"
            }
            },
            "workbench.action.terminal.focus",
            {
            "command": "workbench.action.terminal.sendSequence",
            "args": {
                "text": "python '${file}'\u000D"
            }
            },
            "workbench.action.focusActiveEditorGroup"
        ]
        },
        // 这个和 Ctrl + P 效果是等同的，即，快速搜索打开文件
        {
        "before": [
            "leader",
            "g",
            "g"
        ],
        "commands": [
            {
            "command": "workbench.action.quickOpen"
            }
        ]
        },
        // 在当前打开的项目中搜索文本
        {
        "before": [
            "leader",
            "g",
            "f"
        ],
        "commands": [
            {
            "command": "workbench.view.search"
            }
        ]
        },
    ],
    // vim 的 visual 模式下的键位绑定
    "vim.visualModeKeyBindings": [
        // 向右缩进，可以重复使用
        {
        "before": [
            ">"
        ],
        "commands": [
            "editor.action.indentLines"
        ]
        },
        // 向左缩进，可以重复使用
        {
        "before": [
            "<"
        ],
        "commands": [
            "editor.action.outdentLines"
        ]
        },
    ],
    // vim 的 easymotion 插件的高亮字符的前景色
    "vim.easymotionMarkerForegroundColorOneChar": "#DF5452",
    // 开启 vim-surround
    "vim.surround": true,
    // 修改窗口标题的显示文字
    //   "window.title": "💖${folderName}-FanyFull",
    // 我们在文件管理器中使用 vscode 打开文件时，确保其会在新的 vscode 窗口中打开
    //   "window.openFilesInNewWindow": "on",
    // 将 manifest 文件关联到 xml 文件，这样，manifest 文件就可以使用 xml 的语法高亮了
    "files.associations": {
        "*.manifest": "xml"
    },
}
```
<a name="myu3G"></a>
# 按键绑定 keybindings.json
文件路径： C:\Users\bst\AppData\Roaming\Code\User\keybindings.json
<a name="ZK0zr"></a>
## 自定义快捷键
File > Preferences > Keyboard Shortcuts 进入快捷键设置页面，但我们需要自定义设置，点击下图所示的按钮打开keybindings.json文件<br />![](https://cdn.nlark.com/yuque/0/2023/webp/29305188/1685096574084-e9f711a4-138d-4117-b9d2-2a4c278546a6.webp#averageHue=%23272727&clientId=ue05463c7-790d-4&from=paste&id=u4f483e43&originHeight=328&originWidth=1459&originalType=url&ratio=1.100000023841858&rotation=0&showTitle=false&status=done&style=none&taskId=u295ecc5a-1737-4a85-aa5b-73861ccbe86&title=)<br />我们在keybindings.json文件添加如下内容
```json
// Place your key bindings in this file to override the defaults
// Place your key bindings in this file to override the defaultsauto[]
[
    // new file in explorer
    {
      "key": "ctrl+n",
      "command": "explorer.newFile",
      "when": "explorerViewletFocus"
    },
    // 以下是 vim 绑定的键位
    // 当光标在编辑器中聚焦时，显示和隐藏底部的 panel
    // 会触发 启动 terminal 先关闭
    // {
    //   "key": "ctrl+j",
    //   "command": "workbench.action.togglePanel",
    //   "when": "editorTextFocus"
    // },
    // 编写代码时的智能提示框的上下选择
    // 编写代码时的智能提示框的上下选择
    {
      "key": "ctrl+j",
      "command": "selectNextSuggestion",
      "when": "vim.active && suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
    },
    {
      "key": "ctrl+k",
      "command": "selectPrevSuggestion",
      "when": "vim.active && suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
    },
    // 在 quickOpen 的对话框中上下跳转 即 ctrl+p 模式
    {
      "key": "ctrl+j",
      "command": "workbench.action.quickOpenSelectNext",
      "when": "vim.active && inQuickOpen"
    },
    {
      "key": "ctrl+k",
      "command": "workbench.action.quickOpenSelectPrevious",
      "when": "vim.active && inQuickOpen"
    },
    // 当光标聚焦在编辑器中且 vim 处于 normal 模式时，进行 tab 栏目的左右跳转
    {
      "key": "shift+h",
      "command": "workbench.action.previousEditor",
      "when": "editorTextFocus && vim.mode == 'Normal'"
    },
    {
      "key": "shift+l",
      "command": "workbench.action.nextEditor",
      "when": "editorTextFocus && vim.mode == 'Normal'"
    },
    // 在不同的组件之间进行跳转
    {
      "key": "ctrl+h",
      "command": "workbench.action.navigateLeft"
    },
    {
      "key": "ctrl+l",
      "command": "workbench.action.navigateRight"
    },
    {
      "key": "ctrl+k",
      "command": "workbench.action.navigateUp",
      "when": "terminal.active && terminalFocus"
    },
    // 跳转到 terminal 中
    {
      "key": "ctrl+\\",
      "command": "workbench.action.terminal.toggleTerminal"
    },
    // vim 模式下的左侧的文件管理器的操作
    // 在文件管理器中搜索
    {
      "key": "/",
      "command": "list.find",
      "when": "listFocus && listSupportsFind && !inputFocus"
    },
    // 新建一个文件
    {
      "key": "a",
      "command": "explorer.newFile",
      "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
    },
    // 新建一个文件夹
    {
      "key": "shift+a",
      "command": "explorer.newFolder",
      "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
    },
    // 给文件重命名
    {
      "key": "r",
      "command": "renameFile",
      "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
    },
    // 删除文件
    {
      "key": "d",
      "command": "deleteFile",
      "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
    },
    // 在不同的 terminal 之间进行跳转
    {
      "key": "ctrl+shift+alt+j",
      "command": "workbench.action.terminal.focusNext",
      "when": "terminalFocus && terminalHasBeenCreated && !terminalEditorFocus || terminalFocus && terminalProcessSupported && !terminalEditorFocus"
    },
    {
      "key": "ctrl+shift+alt+k",
      "command": "workbench.action.terminal.focusPrevious",
      "when": "terminalFocus && terminalHasBeenCreated && !terminalEditorFocus || terminalFocus && terminalProcessSupported && !terminalEditorFocus"
    },
    // codeAction 上下选择
    {
      "key": "j",
      "command": "selectNextCodeAction",
      "when": "codeActionMenuVisible"
    },
    {
      "key": "k",
      "command": "selectPrevCodeAction",
      "when": "codeActionMenuVisible"
    },
    // terminal 中上下滚动
    {
      "key": "alt+j",
      "command": "workbench.action.terminal.scrollDown",
      "when": "terminalFocus"
    },
    {
      "key": "alt+k",
      "command": "workbench.action.terminal.scrollUp",
      "when": "terminalFocus"
    },
    // 关闭 terminal
    {
      "key": "ctrl+w",
      "command": "workbench.action.terminal.kill",
      "when": "terminalFocus"
    },
    // 调整底部的 panel 的大小
    {
      "key": "ctrl+shift+k",
      "command": "workbench.action.terminal.resizePaneUp",
      "when": "terminalFocus"
    },
    {
      "key": "ctrl+shift+j",
      "command": "workbench.action.terminal.resizePaneDown",
      "when": "terminalFocus"
    },
    // 最大化 terminal
    {
      "key": "ctrl+win+`",
      "command": "workbench.action.toggleMaximizedPanel",
      "when": "terminalFocus"
    },
  ]

```
