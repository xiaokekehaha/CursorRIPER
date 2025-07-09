![CursorRIPER](../res/github-header.png)
# CursorRIPER 框架 - 安装指南

本指南将帮助您为项目设置CursorRIPER框架。

## 前提条件

- 已安装 [Cursor IDE](https://cursor.sh/)
- Git（可选但建议使用）
- 对项目需求的基本了解

## 安装

1. **复制框架文件到项目并重命名文件为*.mdc**

   在项目根目录创建`.cursor`目录并复制必要文件：

   ```bash
      mkdir -p .cursor/rules
      cp -r /path/to/CursorRIPER/src/.cursor/* .cursor/
      cd .cursor/rules/
      rename 's/\.md$/.mdc/' *.md
   ```

2. **验证安装**

   您的项目现在应该具有以下结构：

   ```
   your-project/
   └── .cursor/
       ├── rules/
       │   ├── core.mdc
       │   ├── state.mdc
       │   ├── start-phase.mdc
       │   ├── riper-workflow.mdc
       │   └── customization.mdc
       └── cursorignore
   ```

## 启动新项目

1. **初始化框架**

   在Cursor IDE中打开您的项目，使用聊天功能初始化框架：

   ```
   /start
   ```

   或者

   ```
   BEGIN START PHASE
   ```

2. **遵循START阶段**

   框架将引导您完成START阶段：

   1. 需求收集
   2. 技术选型
   3. 架构定义
   4. 项目脚手架
   5. 环境设置
   6. 内存库初始化

3. **完成内存库设置**

   确保所有必需的内存文件都已创建并填充：
   
   - `projectbrief.md`
   - `systemPatterns.md`
   - `techContext.md`
   - `activeContext.md`
   - `progress.md`

## 使用RIPER工作流程

完成START阶段后，您将自动过渡到RIPER工作流程。使用以下命令在模式之间切换：

- `/research` 或 `ENTER RESEARCH MODE` - 收集信息并理解现有代码
- `/innovate` 或 `ENTER INNOVATE MODE` - 头脑风暴潜在方法
- `/plan` 或 `ENTER PLAN MODE` - 创建详细的实施计划
- `/execute` 或 `ENTER EXECUTE MODE` - 实施已批准的计划
- `/review` 或 `ENTER REVIEW MODE` - 根据计划验证实施

## 自定义

您可以通过编辑`.cursor/rules/customization.mdc`来自定义框架行为。一些关键设置包括：

- 响应详细程度
- 代码风格偏好
- 内存更新频率
- 自定义命令别名

更多详情请参阅[自定义指南](customization-guide-cn.md)。

## 故障排除

如果您遇到框架问题：

1. 验证所有必需文件存在于`.cursor/rules/`目录中
2. 检查状态不一致性
3. 确保内存库文件存在且格式正确
4. 尝试重启Cursor IDE

如需更多帮助，请参阅[故障排除指南](troubleshooting-guide-cn.md)。

---

*CursorRIPER框架防止编码灾难，同时在会话间保持完美连续性。* 