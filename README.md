# 极简记账 Android APK

## 最简单的构建方式：GitHub 自动构建（推荐，无需安装任何软件）

我已经配置好了 GitHub Actions，代码传到 GitHub 后，云端会自动帮你构建 APK。

### 步骤（约 5 分钟）

1. **注册/登录 GitHub**：打开 [github.com](https://github.com)

2. **创建仓库**：
   - 点击右上角 `+` → **New repository**
   - Repository name 填 `simple-ledger`
   - 点击 **Create repository**

3. **上传代码**：
   - 在新仓库页面，点击 **uploading an existing file**
   - 把本项目所有文件/文件夹拖进去（或点 select files 选择）
   - 注意：需要包含 `.github/workflows/build-apk.yml`
   - 点击 **Commit changes**

4. **等待构建**：
   - 点击上方 **Actions** 标签
   - 看到 `Build APK` 工作流正在运行（约 3-5 分钟）
   - 等状态变成绿色勾勾 ✅

5. **下载 APK**：
   - 点击完成的那次构建记录
   - 页面下方 **Artifacts** 区域，点击 `simple-ledger-apk`
   - 解压下载的 zip，里面的 `app-debug.apk` 就是安装包
   - 传到手机安装即可

---

## 备用方案：Android Studio

如果你以后想改代码或正式发布：

1. 安装 [Android Studio](https://developer.android.com/studio)
2. 打开本项目文件夹
3. 等 Gradle 同步完成
4. Build → Build Bundle(s) / APK(s) → Build APK(s)

APK 输出路径：`app/build/outputs/apk/debug/app-debug.apk`

---

## 项目说明

- 最低支持 Android 7.0（API 24）
- 应用权限：网络访问（加载 CDN 资源）
- 数据完全本地存储，不上传服务器
