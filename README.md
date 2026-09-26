# 德语初学者核心知识手册

单文件 HTML，覆盖 A1–A2 核心语法：字母与发音、W-疑问词、冠词四格、名词单复数、形容词词尾、动词变位、介词支配格、语序。

## 在线访问

GitHub Pages：`https://dahaihh.github.io/<仓库名>/`

## 本地预览

```bash
python3 -m http.server 8000
# 打开 http://127.0.0.1:8000
```

## 结构

| 文件 | 说明 |
|---|---|
| `index.html` | 手册本体，无 JS/CSS 外部依赖，可离线阅读与打印 |
| `audio/` | 83 个发音音频（AAC，约 6 KB/个），点击页面上的 🔊 按需加载 |
| `.nojekyll` | 跳过 Jekyll 构建（避免 GitHub Pages 处理静态资源） |
| `robots.txt` | 阻止搜索引擎索引 |

## 发音音频

第 01 章 30 个字母、第 02 章 53 个例词均可点击朗读，语音由 macOS 德语语音 Anna 生成，经 `afconvert` 压缩为单声道 AAC（32 kbps）。重新生成：

```bash
say -v Anna -o input.aiff "Wasser"
afconvert -f m4af -d aac -b 32000 -c 1 input.aiff audio/wasser.m4a
```

## 打印

浏览器 Cmd/Ctrl + P 可直接导出 PDF（已内置 A4 打印样式）。
