## [1.3.3](https://github.com/tsukimiya-wk/git-project-common-configuration/compare/v1.3.2...v1.3.3) (2025-04-28)


### Bug Fixes

* **github actions:** 修复github-actions[bot]没有权限的问题 ([81cf7c3](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/81cf7c3f1eb63fa5337162be4945d8d91266fba9))

## [1.3.2](https://github.com/tsukimiya-wk/git-project-common-configuration/compare/v1.3.1...v1.3.2) (2025-04-28)


### Bug Fixes

* **github actions:** 修复merge任务问题 ([0e8754e](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/0e8754eb6e3c48df068d62ec1cdb14c7c2ebdcf2))

## [1.3.1](https://github.com/tsukimiya-wk/git-project-common-configuration/compare/v1.3.0...v1.3.1) (2025-04-28)


### Bug Fixes

* **github actions:** 修复merge任务不在git文件夹里的问题 ([0f44445](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/0f444450c583d113a5f9268901b2c8e1acad3304))

# [1.3.0](https://github.com/tsukimiya-wk/git-project-common-configuration/compare/v1.2.0...v1.3.0) (2025-04-28)


### Features

* **github actions:** 将release.yaml分成两个任务，避免合并后develop存在提交落后于main分支的情况 ([ae4db14](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/ae4db1483edd1812b15bf009061ed01ad64e5577))

# [1.2.0](https://github.com/tsukimiya-wk/git-project-common-configuration/compare/v1.1.0...v1.2.0) (2025-04-28)


### Features

* **github actions:** 移除了release.yaml里的条件部分，在合并develop到main后强制合并main到develop，避免出现develop落后于main的情况 ([7e16b35](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/7e16b3561bc0858edead144d79e89fd60ca58950))

# [1.1.0](https://github.com/tsukimiya-wk/git-project-common-configuration/compare/v1.0.2...v1.1.0) (2025-04-28)


### Features

* **test:** 假设的新功能1 ([607d2ae](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/607d2aec78d2327646fb1956ba5956d99a06b18c))
* **test:** 假设的新功能2 ([3ebed55](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/3ebed5566b1fc672121dd1a58e88b4cfa0f2a9de))

## [1.0.2](https://github.com/tsukimiya-wk/git-project-common-configuration/compare/v1.0.1...v1.0.2) (2025-04-28)


### Bug Fixes

* **github actions:** 修复预发布分支错误问题 ([b13421d](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/b13421d4867ed9e9c096fa8cbfe7379ac9289771))

## [1.0.1](https://github.com/tsukimiya-wk/git-project-common-configuration/compare/v1.0.0...v1.0.1) (2025-04-28)


### Bug Fixes

* **github actions:** 修复npm clean-install 包错问题 ([2804b57](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/2804b5776e17f2ad42d06f41a2426b10f2065f90))
* **github actions:** 修复semantic-release在拉取请求时不会生成版本号的问题 ([64d03f6](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/64d03f6b4f777df54a20082d57a83ba9c2115fde))
* 修复因合并问题导致REAME内容消失的问题 ([a93a5db](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/a93a5dbe3e16a354177ab638d227bcafb1662b1f))

## [1.0.1-develop.1](https://github.com/tsukimiya-wk/git-project-common-configuration/compare/v1.0.0...v1.0.1-develop.1) (2025-04-27)


### Bug Fixes

* 修复因合并问题导致REAME内容消失的问题 ([a93a5db](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/a93a5dbe3e16a354177ab638d227bcafb1662b1f))

# 1.0.0 (2025-04-27)


### Bug Fixes

* **ci:** 修复自动化生成版本 ([5d4d049](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/5d4d0495c109df522727880c71b4a128163687e5)), closes [#4](https://github.com/tsukimiya-wk/git-project-common-configuration/issues/4)
* **release:** 修复了.releaserc配置文件的错误 ([55f38f8](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/55f38f8d44514cdf518ab585bf99b369a70929bd))
* 修复GitHub Actions 权限问题 ([730a5f7](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/730a5f7a1e75822bee7835e61f7db76d461af032))
* 修复了非交互式环境下执行脚本的问题 ([dc0ae76](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/dc0ae76b0cab5cc5f0d7deab864e82d437a08793))
* 修复了非交互式终端环境里运行"exec < /dev/tty"报错问题 ([00daa4e](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/00daa4ebf3a2d0e5f72974eaaa28bf9b676ec2f3))


### Features

* 自动化生成语义版本 ([5584ecc](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/5584eccaaadac9d0b5557808ef47a54c0ee312d3))

# 1.0.0-develop.1 (2025-04-27)


### Bug Fixes

* **ci:** 修复自动化生成版本 ([5d4d049](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/5d4d0495c109df522727880c71b4a128163687e5)), closes [#4](https://github.com/tsukimiya-wk/git-project-common-configuration/issues/4)
* **release:** 修复了.releaserc配置文件的错误 ([55f38f8](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/55f38f8d44514cdf518ab585bf99b369a70929bd))
* 修复GitHub Actions 权限问题 ([730a5f7](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/730a5f7a1e75822bee7835e61f7db76d461af032))
* 修复了非交互式环境下执行脚本的问题 ([dc0ae76](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/dc0ae76b0cab5cc5f0d7deab864e82d437a08793))
* 修复了非交互式终端环境里运行"exec < /dev/tty"报错问题 ([00daa4e](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/00daa4ebf3a2d0e5f72974eaaa28bf9b676ec2f3))


### Features

* 自动化生成语义版本 ([5584ecc](https://github.com/tsukimiya-wk/git-project-common-configuration/commit/5584eccaaadac9d0b5557808ef47a54c0ee312d3))
