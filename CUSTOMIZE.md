# 把本站改成你自己的 — 定制清单

按下面逐项替换，就能把 clone 来的模板变成你的个人主页。

---

## 1. 站点基本信息

**文件：`config/_default/config.toml`**

| 项 | 说明 | 建议 |
|----|------|------|
| `baseurl` | 站点根地址 | 仓库为 `tianming23.github.io` 时保持 `https://tianming23.github.io/`；若是子目录如 `blog`，改为 `https://tianming23.github.io/blog/` |
| `title` | 浏览器标题、站点名 | 改成你的博客名或昵称 |
| `languageCode` / `defaultContentLanguage` | 默认语言 | 中文用 `zh-cn`，英文用 `en` |
| `disqusShortname` | Disqus 评论 | 不用就留空 `""` |

已按「tianming23.github.io + 中文」预改过，你只需确认或微调。

---

## 2. 头像与副标题（侧边栏）

**文件：`config/_default/params.toml`**

- **`[sidebar]`**
  - `subtitle`：侧边栏一句话介绍，改成你的简介或座右铭。
  - `emoji`：侧边栏小图标，可改成任意 emoji。
  - `avatar`：头像路径，保持 `img/avatar.png` 即可。

**头像文件位置：**

- 把你的头像放到 **`assets/img/avatar.png`**（推荐），或 **`static/img/avatar.png`**，覆盖原有文件。
- 建议尺寸：正方形，约 200×200 像素以上。

**Favicon（浏览器小图标）：****

- 同目录下 `favicon.png` 放在 `assets/img/favicon.png` 或 `static/img/favicon.png`，在 `params.toml` 里已配置为 `favicon = "img/favicon.png"`。

---

## 3. 社交链接（侧边栏图标）

**文件：`config/_default/menu.toml`**

- 已把 GitHub 改成 `https://github.com/tianming23`，请确认是否你的账号。
- 需要更多链接：复制一段 `[[social]]`，改 `identifier`、`name`、`url` 和 `icon`（图标名见主题文档）。
- 不需要的链接：整段用 `#` 注释掉或删掉。

---

## 4. 页脚

**文件：`config/_default/params.toml`**

- `[footer]` → `since`：建站年份，已改为 2025，可按需改。
- `customText`：页脚多出来的自定义文字（如备案号、版权说明），不需要就留空 `""`。

---

## 5. 内容：删示例、写自己的

- **首页**：`content/_index.md` 目前只有菜单配置，首页列表由「文章」自动生成。
- **文章**：在 `content/post/` 下：
  - 删掉示例文章（如 `hello-world`、`markdown-syntax` 等），或保留当参考。
  - 新建文件夹如 `content/post/我的第一篇文章/index.md`，写你的文章。
- **分类 / 标签**：在文章 front matter 里写 `categories`、`tags`，会自动生成分类页；示例分类在 `content/categories/example-category/`，可改名或删掉。
- **链接页**：`content/page/links/index.md` 里 `links` 改成你自己的友链或常用链接。

---

## 6. 评论（可选）

**文件：`config/_default/params.toml`**

- `[comments]`：当前是 Disqus。若不用评论，可设 `enabled = false`。
- 若要用其他评论（如 Giscus、Utterances），需在主题文档里查对应配置并改这里。

---

## 7. 本地预览

在项目根目录执行：

```bash
hugo server
```

浏览器打开 `http://localhost:1313`，改完配置或内容后刷新即可看效果。

---

## 8. 部署到 GitHub Pages

- 仓库名是 `tianming23.github.io` 时，推送后 GitHub Actions 会自动构建并发布。
- 在仓库 **Settings → Pages** 里，**Source** 选 **GitHub Actions**（模板已配好 workflow）。

改完上述项并推送到 GitHub，站点就会变成「你的」内容与身份。
