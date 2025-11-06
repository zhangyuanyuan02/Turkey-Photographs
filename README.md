# Turkey-Photographs

土耳其旅行照片汇总仓库

## 📁 文件夹结构

本仓库包含五个文件夹，每个文件夹以团队成员的名字命名：

- **DJR** - DJR 的旅行照片
- **WJK** - WJK 的旅行照片
- **XJQ** - XJQ 的旅行照片
- **ZQK** - ZQK 的旅行照片
- **ZZY** - ZZY 的旅行照片

每个成员可以在自己的文件夹中上传和整理土耳其旅行的照片。

## 🚀 如何贡献

### 1. Fork 仓库

首先，你需要将这个仓库 fork 到你自己的 GitHub 账号下：

1. 点击页面右上角的 **Fork** 按钮
2. 选择你的 GitHub 账号作为目标账号
3. 等待 fork 完成

### 2. 克隆你 fork 的仓库

将你 fork 的仓库克隆到本地计算机：

```bash
# 将 YOUR_USERNAME 替换为你的 GitHub 用户名
git clone https://github.com/YOUR_USERNAME/Turkey-Photographs.git
cd Turkey-Photographs
```

### 3. 配置上游仓库

为了能够同步原始仓库的更新，需要添加上游仓库（upstream）：

```bash
# 添加原始仓库为上游远程仓库
git remote add upstream https://github.com/zhangyuanyuan02/Turkey-Photographs.git

# 验证远程仓库配置
git remote -v
```

你应该看到类似以下输出：
```
origin    https://github.com/YOUR_USERNAME/Turkey-Photographs.git (fetch)
origin    https://github.com/YOUR_USERNAME/Turkey-Photographs.git (push)
upstream  https://github.com/zhangyuanyuan02/Turkey-Photographs.git (fetch)
upstream  https://github.com/zhangyuanyuan02/Turkey-Photographs.git (push)
```

### 4. 创建新分支

在进行任何更改之前，创建一个新的分支：

```bash
# 创建并切换到新分支
git checkout -b add-my-photos
```

### 5. 添加你的照片

将你的照片添加到对应的文件夹中：

```bash
# 例如，如果你是 DJR，将照片复制到 DJR 文件夹
cp /path/to/your/photos/* DJR/

# 添加文件到 git
git add DJR/

# 提交更改
git commit -m "添加 DJR 的土耳其旅行照片"
```

### 6. 推送到你的 fork

将更改推送到你 fork 的仓库：

```bash
git push origin add-my-photos
```

### 7. 创建 Pull Request

1. 访问你 fork 的仓库页面（https://github.com/YOUR_USERNAME/Turkey-Photographs）
2. 点击 **Pull Request** 标签
3. 点击 **New Pull Request** 按钮
4. 确保：
   - Base repository: `zhangyuanyuan02/Turkey-Photographs`
   - Base: `main`
   - Head repository: `YOUR_USERNAME/Turkey-Photographs`
   - Compare: `add-my-photos`
5. 填写 Pull Request 的标题和描述
6. 点击 **Create Pull Request** 按钮

## 🔄 如何同步仓库版本

当原始仓库有更新时，你需要同步这些更改到你的 fork：

### 方法一：使用命令行

```bash
# 1. 确保你在主分支上
git checkout main

# 2. 从上游仓库获取最新更改
git fetch upstream

# 3. 合并上游的更改到你的本地主分支
git merge upstream/main

# 4. 推送更新到你的 fork
git push origin main
```

### 方法二：使用 GitHub 网页界面

1. 访问你 fork 的仓库页面
2. 如果你的 fork 落后于原始仓库，会看到提示信息："This branch is X commits behind zhangyuanyuan02:main"
3. 点击 **Sync fork** 按钮
4. 点击 **Update branch** 按钮

### 在工作分支中同步最新更改

如果你正在一个功能分支上工作，想要同步主分支的最新更改：

```bash
# 1. 先同步主分支（按上面的步骤）
git checkout main
git fetch upstream
git merge upstream/main
git push origin main

# 2. 切换回你的工作分支
git checkout add-my-photos

# 3. 将主分支的更改合并到工作分支
git merge main

# 4. 如果有冲突，解决冲突后提交
git add .
git commit -m "合并主分支的最新更改"

# 5. 推送到你的 fork
git push origin add-my-photos
```

## 📝 最佳实践

1. **定期同步**：在开始新工作之前，先同步上游仓库的最新更改
2. **使用分支**：始终在新分支上进行更改，不要直接在 main 分支上工作
3. **提交信息**：编写清晰的提交信息，说明你做了什么更改
4. **照片命名**：建议使用有意义的文件名，如 `伊斯坦布尔-蓝色清真寺.jpg`
5. **文件大小**：注意照片文件大小，建议压缩后再上传（GitHub 单个文件限制 100MB）
6. **尊重他人文件夹**：只在自己的文件夹中添加或修改照片

## 🎯 快速参考

### 第一次设置
```bash
# Fork 仓库（在 GitHub 网页上操作）
# 然后克隆和配置
git clone https://github.com/YOUR_USERNAME/Turkey-Photographs.git
cd Turkey-Photographs
git remote add upstream https://github.com/zhangyuanyuan02/Turkey-Photographs.git
```

### 日常工作流程
```bash
# 1. 同步最新更改
git checkout main
git fetch upstream
git merge upstream/main
git push origin main

# 2. 创建新分支并工作
git checkout -b my-new-photos
# ... 添加照片 ...
git add .
git commit -m "描述你的更改"
git push origin my-new-photos

# 3. 在 GitHub 上创建 Pull Request
```

## ❓ 遇到问题？

如果你在使用过程中遇到问题，可以：

1. 查看 [GitHub 官方文档](https://docs.github.com/cn)
2. 在仓库中创建 Issue 寻求帮助
3. 联系团队其他成员

祝大家使用愉快！🎉