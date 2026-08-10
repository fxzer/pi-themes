# pi-themes · Vitesse Custom

为 [Pi Coding Agent](https://pi.dev) 移植的 **Vitesse Custom** 配色主题，包含深色与浅色两套，基于个人在 Zed 中的 `vitesse-custom` 定制配色改编。

## 包含的主题

| 文件 | 主题名 | 适用 |
|---|---|---|
| `vitesse-custom-dark.json` | `vitesse-custom-dark` | 深色模式 |
| `vitesse-custom-light.json` | `vitesse-custom-light` | 浅色模式 |

## 安装

将主题文件放入 pi 的主题目录，或直接把本仓库目录加入 `themes` 配置：

```bash
# 方式一：拷贝文件
cp vitesse-custom-*.json ~/.pi/agent/themes/

# 方式二：在 settings.json 中指向本仓库目录
# "themes": ["/path/to/pi-themes"]
```

然后在 `~/.pi/agent/settings.json` 中选择主题：

```json
{
  "theme": "vitesse-custom-dark"
}
```

## 跟随系统深浅色

配合 [pi-system-theme](https://www.npmjs.com/package/pi-system-theme) 扩展自动切换：

```bash
pi install npm:pi-system-theme
```

在 `~/.pi/agent/system-theme.json` 中配置：

```json
{
  "darkTheme": "vitesse-custom-dark",
  "lightTheme": "vitesse-custom-light"
}
```

## 状态栏配色

配合 [pi-statusline](https://www.npmjs.com/package/@narumitw/pi-statusline) 扩展，
`pi-statusline.json` 提供一套与主题同源的绿色渐变调色板。

```bash
pi install npm:@narumitw/pi-statusline
```

安装后将本仓库的 `pi-statusline.json` 复制到 `~/.pi/agent/pi-statusline.json`，
或直接使用其中的 `palette` 配置，重启 pi 生效。

## 配色说明

- 深色版：背景 `#121212`，主色绿 `#52c892`，正文 `#dbd7ca`
- 浅色版：背景 `#ffffff`，主色绿 `#369b60`，正文 `#393a34`
- 完整覆盖 pi 主题规范的 51 个必需 token（含 2 个可选 token），包括 UI、Markdown、代码高亮、diff、思考等级边框

颜色参考自 [Vitesse](https://github.com/antfu/vitesse) 系列配色（MIT），个人定制版见 Zed 配置。

## License

MIT
