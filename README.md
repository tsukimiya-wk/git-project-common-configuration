# git-project-common-configuration

git 项目通用配置

## 基本配置

| 工具             | 描述                                                                                    | 相关插件                                    | 配置文件                                   |
| ---------------- | --------------------------------------------------------------------------------------- | ------------------------------------------- | ------------------------------------------ |
| commitlint       | 用于 git commit 格式校验                                                                | 无                                          | commitlint.config.js                       |
| commitizen       | 用于 git commit 交互式提交                                                              | cz-conventional-changelog                   | .czrc                                      |
| lint-staged      | 用于 git commit 提交前进行文件格式校验                                                  | 需要格式校验的文件对应的工具，比如 prettier | .lintstagedrc                              |
| prettier         | 格式化文件工具                                                                          |                                             | .prettierrc                                |
| husky            | Git 钩子开发工具，配合其他工具，能在提交/推送前自动检查提交信息、格式化代码、运行测试等 | commitlint，commiizen，lint-staged,等等     | 参考 `husky 配置` 部分                     |
| semantic-release | 语义化版本管理                                                                          | @semantic-release/\*                        | .releaserc，.github/workflows/release.yaml |
| .editorconfig    | 编辑器配置文件                                                                          | 无                                          | .editorconfig                              |

### 安装命令

```bash
pnpm i -D -E prettier
pnpm i -D lint-staged
pnpm i -D @commitlint/cli @commitlint/config-conventional
pnpm i -D commitizen
pnpm i -D -E cz-conventional-changelog
pnpm dlx husky-init && pnpm i
pnpm i -D semantic-release @semantic-release/commit-analyzer @semantic-release/release-notes-generator @semantic-release/changelog @semantic-release/git @semantic-release/github
```

如果要发布到 npm，还需要安装 `@semantic-release/npm`

**注意**：

命令 `pnpm dlx husky-init` 无法在 MacOS 创建文件夹，可以先手动创建 `.husky` 文件夹，再执行该命令

### husky 配置

下列钩子的执行顺序为: `pre-commit` -> `prepare-commit-msg` -> `commit-msg`

```bash
# 在提交信息之前，先运行 lint-staged
npx husky add .husky/pre-commit "npx lint-staged"

# 使用 commitlint 检查提交信息
# 必须使用双引号包裹住 $1
npx husky add .husky/commit-msg 'npx --no -- commitlint --edit "$1"'

# 使用 commitizen 代替 git commit
npx husky add .husky/prepare-commit-msg "exec < /dev/tty && npx cz --hook || true"
```

在CI/CD，GitHub Actions 等非交互式终端下，需要添加下列代码

```bash
if [ -t 1 ]; then
    # 仅在交互式终端中执行的命令
else
    exit 0
fi
```
