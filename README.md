# 个人资源

主要是博客图片

原仓库名为 `blogPic`，2026.05.31 精简为 `r`(resource)

分支名精简为 `m`(main 或 master)

* [个人笔记](https://github.com/baiqiantao/qtNotes)
* [为知笔记](https://github.com/baiqiantao/wizNote)
* [博客图片](https://github.com/baiqiantao/blogPic)

## 旧链接兼容性说明

仓库改名（`blogPic` → `r`）和分支精简（`master`/`main` → `m`）后，以下几种格式的链接均可正常访问：

| 格式        | 链接                                                                                       | 状态  |
|-----------|------------------------------------------------------------------------------------------|-----|
| 旧仓库 + 旧分支 | https://raw.githubusercontent.com/baiqiantao/blogPic/master/img/2024/202503282223862.png | 可访问 |
| 旧仓库 + 新分支 | https://raw.githubusercontent.com/baiqiantao/blogPic/m/img/2024/202503282223862.png      | 可访问 |
| 新仓库 + 旧分支 | https://raw.githubusercontent.com/baiqiantao/r/master/img/2024/202503282223862.png       | 可访问 |
| 新仓库 + 新分支 | https://raw.githubusercontent.com/baiqiantao/r/m/img/2024/202503282223862.png            | 可访问 |

**实现原理**

* **仓库名重定向**：GitHub 在仓库改名时，会在数据库中永久保存旧名到新名的映射。所有对旧仓库名的请求（API、raw 文件、clone 等）都会被自动重定向到新仓库，无需额外配置。
* **分支 fallback**：GitHub 的 `raw.githubusercontent.com` 服务在处理请求时，如果 URL 中指定的分支不存在（如已删除的 `master`），会自动回退到仓库的默认分支（当前为 `m`）。因此即使分支已删除，只要文件在默认分支中存在，旧链接依然有效。

