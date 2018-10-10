## 这是我配置的 Sublime Texe3 集成插件包，linux版，windows可能有的插件不太兼容，我比较喜欢简洁，所以界面不是很华丽，上图吧![Alt text](https://raw.githubusercontent.com/achuanya/packages/master/image/sublime.png "sublime")

## 含插件如下：

 * AngularJS
 * AutoFileName
 * Boxy Theme
 * Localinzation
 * Color Highlight      //插件需要配置一下，下面会讲到
 * Colorsublime
 * DocBlockr            //插件需要配置一下，下面会讲到
 * Emmet
 * Material Theme
 * Package Control
 * Themr
 * View inBrowser
 * ConvertToUTF-8
 * LiveReload
 * SublimeTmpl
 * ColorPicker
 * SublimeLinter

## 配置

### Color Highlight 配置

        Preferences -> Package Settings -> Color Highlighter -> Settings - User,

        // 配置成如下内容： 

        {
        "search_colors_in": {
            "all_content": {
                "enabled": true,
                "color_highlighters": {
                    "color_scheme": {
                        // 主要是修改这两项
                        "enabled": true,
                        "highlight_style": "filled" // 填充的意思
                        }
                    }
                }
            }
        } 然后重启 Sublime 就可以了。

### CDocBlockr 配置
 
            Preferences -> Package Settings -> DocBlockr -> Settings - User,

        // 配置成如下内容：

        {
        "jsdocs_extra_tags":[
            "@Author Hybrid",
            "@DateTime ",
            "@copyright ${1:[copyright]}",
            "@license ${1:[license]}",
            "@version ${1:[version]}"
        ],
        "jsdocs_function_description": false   }

### 个人用户设置

我不太喜欢代码提示就给关了，需要用的话注释掉就可以  

            {
            "auto_complete": false,　　//关闭代码提示
            "color_scheme": "Packages/colorsublime- theme/Active4D.tmTheme",
            "command": "open_in_browser",
            "font_face": "Source Code Pro, 'Courier New', monspace",
            "font_size": 11,
            "ignored_packages":
            [
                "Vintage"
            ],
            "keys":
            [
                "alt+shlft+z"
            ],
            "theme": "Boxy Yesterday.sublime-theme"

        }

值得一提的是字体！＂Source Code Pro＂
号称最美编程字体Adobe旗下一款开源字体,下面咱们开始安装

### cp TTF文件夹下的内容到 /usr/share/fonts/truetype/ 目录

        sudo cp -r source-code-pro/TTF/ /usr/share/fonts/truetype/source-code-pro

### 再执行

        $ sudo fc-cache -f -v

完成后就可以使用它了!

