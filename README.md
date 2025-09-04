<!--
 * @Author: @ydzat
 * @Date: 2025-09-04 20:46:02
 * @LastEditors: @ydzat
 * @LastEditTime: 2025-09-04 20:52:18
 * @Description: 
-->
# AI-IDE 插件市场

这是AI-IDE的官方插件市场仓库，管理所有已注册的插件信息。

## 📋 插件提交流程

### 1. 准备你的插件

确保你的插件仓库包含：
- `package.json` - 包含插件的基本信息
- `README.md` - 插件使用说明
- 完整的插件代码

### 2. 提交插件到市场

1. 在本仓库创建一个新的Issue
2. 选择"插件提交"模板
3. 填写你的插件仓库链接
4. 等待管理员审核

### 3. 自动化流程

审核通过后，系统将自动：
- 分配唯一的AppID
- 更新插件注册表
- 关闭Issue并通知结果

## 🏗️ 插件注册表结构

```json
{
  "version": "1.0.0",
  "lastUpdated": "2025-09-04T18:30:00Z",
  "nextAppId": 2,
  "plugins": {
    "1": {
      "appId": "1",
      "repository": "https://github.com/username/plugin-repo.git",
      "submittedBy": "username",
      "submittedAt": "2024-01-01T00:00:00Z",
      "status": "approved",
      "approvedBy": "admin",
      "approvedAt": "2024-01-01T12:00:00Z"
    }
  }
}
```

## 🔧 插件开发规范

### package.json 要求

```json
{
  "name": "your-plugin-name",
  "displayName": "Your Plugin Display Name",
  "description": "Plugin description",
  "version": "1.0.0",
  "publisher": "your-name",
  "appId": "1",
  "categories": ["Other"],
  "keywords": ["keyword1", "keyword2"],
  "main": "./extension.js",
  "activationEvents": ["onStartupFinished"],
  "contributes": {
    "commands": [
      {
        "command": "your-plugin.command",
        "title": "Command Title"
      }
    ]
  }
}
```

## 📊 市场统计

- 总插件数：1
- 活跃插件：1
- 最后更新：2025-09-04

## 🤝 贡献指南

1. Fork 本仓库
2. 创建功能分支
3. 提交更改
4. 创建Pull Request

## 📞 联系我们

如有问题，请：
- 创建Issue
- 联系维护者

---

**注意**：此仓库仅存储插件注册信息，插件的详细信息（名称、描述、版本等）将从各插件的GitHub仓库动态获取。