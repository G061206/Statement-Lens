# Statement Lens · 账单透镜

独立第三方的本地报表分析工具。此目录是重新建立项目的可运行底稿，暂用 Statement Lens 作为产品名称。

它由独立开发者提供，与 Interactive Brokers 无隶属、授权或背书关系，不是券商官方网站。

项目仓库：[G061206/Statement-Lens](https://github.com/G061206/Statement-Lens)。

## 本地使用

需要 Node.js 22 或更新版本，无需安装依赖。

```powershell
git clone https://github.com/G061206/Statement-Lens.git
cd Statement-Lens
npm run serve
```

打开 http://127.0.0.1:4188/ ，点击「载入示例」即可查看演示。

```powershell
npm run check
npm test
```

## 功能与兼容格式

保留账户总览、持仓、收益、每日统计、数据质量、中英文界面、浅色/暗色主题、多个周期报表合并、JSON 导出和横/竖版分享图。

当前解析器仅兼容 Interactive Brokers 导出的中文或英文 Activity Statement CSV/TXT，不代表支持所有券商。券商名称仅用于说明格式兼容性和第三方身份，不用作产品名称或标识。本工具不收集券商账号、密码或验证码。

报表在当前浏览器内处理，不上传到服务器。浏览器本地存储仅保留语言、主题和分享偏好。所有指标都应与原始报表核对。

## 重建边界

- 产品名、页面标题、图标、导航、下载文件名和分享图使用独立名称与新设计的文档透镜标记，按用户要求保留原红黑配色。
- 没有复制旧 Logo、旧域名、旧仓库链接、部署配置、Git 历史、宣传材料或截图。
- 按用户要求移除首页和分析页面的独立身份说明栏目；分享图左下角使用 `GitHub/Statement Lens`，首页页脚保留简短的第三方身份文字。
- 示例是演示数据，券商名称改为 Synthetic Demo Data，移除券商地址、官方法律文本和代码释义；示例中的券商股票改为 DEMO。
- 内部解析函数中的 `Ibkr` 表示报表格式，不作为公开品牌；旧代码的 MIT 版权声明完整保留在 LICENSE 中。
- 当前仅提供本地运行底稿，没有发布或替换公网网站，robots 与 HTML 暂时禁止搜索索引。

重建清单见 [docs/REBUILD.md](docs/REBUILD.md)。
