# 使用GitHub Desktop推送代码

## 📥 第一步：下载并安装GitHub Desktop

### 下载地址
https://desktop.github.com/

点击下载按钮，安装到电脑上（大约100MB，安装只需1-2分钟）。

---

## 🔐 第二步：登录GitHub账号

1. 打开GitHub Desktop
2. 点击 **"Sign in to GitHub.com"**
3. 在浏览器中登录你的GitHub账号
4. 授权GitHub Desktop访问权限
5. 点击 **"Authorize desktop"**

✅ 登录成功后会自动返回GitHub Desktop

---

## 📂 第三步：添加现有仓库

1. 点击左上角 **"File"** → **"Add local repository"**
2. 点击 **"Choose..."** 按钮
3. 浏览到你的项目文件夹：`E:\icc_gv`
4. 点击 **"Add repository"**

✅ 现在你应该能看到仓库名称：**ICC-GVLTS-Educational-System**

---

## 🚀 第四步：推送到GitHub

1. 在GitHub Desktop中间区域，你会看到：
   - 左侧：16个文件的变更列表
   - 右侧：文件内容预览

2. 确认这些文件已经被提交（左下角显示提交历史）

3. 点击顶部的 **"Publish repository"** 按钮
   - 或者如果是 **"Push origin"** 按钮，直接点击

4. 在弹出窗口中：
   - ✅ 确保 **"Keep this code private"** 是 **未勾选** 状态（公开仓库）
   - 点击 **"Publish repository"** 确认

5. 等待上传完成（约60MB音频文件，可能需要2-5分钟）

---

## ✅ 第五步：验证推送成功

### 方法一：在GitHub Desktop中确认
- 顶部状态栏显示 "Last fetched just now"
- 没有"Push origin"按钮（说明已同步）

### 方法二：在GitHub网站确认
1. 打开浏览器访问：
   ```
   https://github.com/Halienzo/ICC-GVLTS-Educational-System
   ```

2. 你应该能看到：
   - ✅ index.html 文件
   - ✅ 所有.mp3和.mid文件
   - ✅ README.md
   - ✅ 16 commits（或类似数字）

---

## 🌐 第六步：回到Netlify继续部署

推送成功后：

1. 回到Netlify网页（刷新页面如果需要）
2. 重新选择你的仓库进行部署
3. 现在 **"Branch to deploy"** 下拉菜单应该有选项了！
4. 选择 **`master`** 分支
5. 点击 **"Deploy site"**

🎉 **完成！**

---

## 🔄 后续更新流程（超简单）

以后修改代码后，只需要：

1. 打开GitHub Desktop
2. 它会自动检测到文件变更
3. 在左下角输入提交描述（如 "修复bug"）
4. 点击 **"Commit to master"**
5. 点击 **"Push origin"**

Netlify会自动检测并重新部署！✨

---

## ⚠️ 常见问题

### Q: 推送很慢？
A: 首次推送60MB文件确实需要时间，请耐心等待。可以查看GitHub Desktop底部的进度条。

### Q: 推送失败显示网络错误？
A: 检查网络连接，或稍后重试。GitHub Desktop会自动重试失败的推送。

### Q: 看不到"Publish repository"按钮？
A: 说明可能已经推送过了。点击顶部的 **"Repository"** → **"Push"** 强制推送。

---

**祝部署顺利！🚀**
