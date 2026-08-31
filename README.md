# Pocket Docs (Mintlify)

这是给 [Mintlify](https://mintlify.com) 用的文档仓库根目录。Mintlify **不支持 zip 导入**，要连 GitHub 仓库。

## 在 Mintlify 控制台接入

1. 新建一个 **空的 GitHub 仓库**（建议名 `pocket-docs`），只放本目录里的文件，不要带外层 `docs-mintlify-pocket/` 文件夹。
2. 打开 [Mintlify dashboard](https://dashboard.mintlify.com) → Create project / Connect GitHub。
3. 选中该仓库，文档根目录填 `/`（仓库根就是 `docs.json`）。
4. 自定义域名绑 `docs.pocket.fi`。

把本目录推上去的最快做法：

```bash
cd docs-mintlify-pocket
git init -b main
git add .
git commit -m "Initial Pocket docs"
git remote add origin git@github.com:<你的账号>/pocket-docs.git
git push -u origin main
```

## 本地预览

```bash
cd docs-mintlify-pocket
npx mint dev
```

浏览器打开 `http://localhost:3000`。

## 和 GitBook 源的关系

内容从 `docs-gitbook-pocket/` 转换而来。之后改文档以本目录为准（Mintlify 真源）。
