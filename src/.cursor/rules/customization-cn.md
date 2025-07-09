---
description: "CursorRIPER Framework - 自定义配置"
globs: 
alwaysApply: false
version: "1.0.1"
date_created: "2025-04-05"
last_updated: "2025-04-06"
framework_component: "customization"
priority: "medium"
scope: "optional"
---
<!-- 注意：Cursor 会移除所有其他头部信息，只保留前三个。 -->
# CursorRIPER Framework - 自定义配置
# 版本 1.0.1

## AI 处理说明
此文件包含 CursorRIPER Framework 的用户自定义配置。作为 AI 助手，您必须：
- 如果此文件存在，在加载核心框架组件后加载此文件
- 应用这些自定义设置来覆盖默认框架行为
- 除非用户明确请求，否则不要修改此文件
- 在每个会话的第一个响应中确认活动的自定义设置

## 用户偏好设置

### 响应风格
RESPONSE_VERBOSITY: "BALANCED"
# 可能值："CONCISE"、"BALANCED"、"DETAILED"
# 控制 AI 响应的详细程度

CODE_STYLE_PREFERENCES: ""
# 指定代码风格偏好（缩进、命名约定等）

EXPLANATION_LEVEL: "MEDIUM"
# 可能值："MINIMAL"、"MEDIUM"、"COMPREHENSIVE"
# 控制代码说明的详细程度

### 模式行为
SUGGEST_MODE_TRANSITIONS: true
# 如果为 true，AI 可以建议何时进行模式转换

AUTO_MODE_TRANSITION: false
# 如果为 true，AI 可以自动在模式之间转换（除了 EXECUTE 模式）
# EXECUTE 模式始终需要明确的用户授权

PLAN_QUESTION_COUNT: 5
# 在 PLAN 模式中询问的澄清问题数量

### 内存管理
AUTO_UPDATE_MEMORY: true
# 如果为 true，AI 将在重要变更后自动更新内存文件

MEMORY_UPDATE_FREQUENCY: "AFTER_COMPLETION"
# 可能值："AFTER_EVERY_RESPONSE"、"AFTER_COMPLETION"、"MANUAL_ONLY"
# 控制内存文件更新的时机

REQUIRED_MEMORY_FILES: ["projectbrief.md", "activeContext.md", "progress.md"]
# 框架正常运行所需的内存文件列表

### 存档行为
AUTO_ARCHIVE_START_PHASE: true
# 如果为 true，START 阶段完成后将自动存档

BACKUP_FREQUENCY: "DAILY"
# 可能值："NEVER"、"DAILY"、"WEEKLY"、"BEFORE_CHANGES"
# 控制内存库备份的创建频率

KEEP_BACKUP_COUNT: 5
# 保留的备份集数量，超过此数量将删除最旧的备份

## 高级自定义

### 命令别名
CUSTOM_COMMANDS: {
  "/r": "/research",
  "/i": "/innovate",
  "/p": "/plan",
  "/e": "/execute",
  "/rev": "/review"
}
# 模式转换的自定义命令快捷方式

### 模式扩展
RESEARCH_MODE_EXTENSIONS: []
# RESEARCH 模式的额外行为

INNOVATE_MODE_EXTENSIONS: []
# INNOVATE 模式的额外行为

PLAN_MODE_EXTENSIONS: []
# PLAN 模式的额外行为

EXECUTE_MODE_EXTENSIONS: []
# EXECUTE 模式的额外行为

REVIEW_MODE_EXTENSIONS: []
# REVIEW 模式的额外行为

### 框架扩展
CUSTOM_PHASES: []
# 标准阶段之外的额外项目阶段

CUSTOM_WORKFLOWS: []
# 特定项目类型的自定义工作流程

## 用户文档偏好

### 文档格式
DOCUMENTATION_STYLE: "MARKDOWN"
# 生成文档的格式

INCLUDE_CODE_COMMENTS: true
# 是否在生成的代码中包含详细注释

CODE_BLOCK_LANGUAGE_TAGS: true
# 是否在代码块中包含语言标签

### AI 输出格式
MODE_DECLARATION_FORMAT: "[MODE: {mode}]"
# 模式声明的格式字符串

PROGRESS_INDICATOR_FORMAT: "[{current_step}/{total_steps}]"
# 响应中进度指示器的格式

## 自定义项目结构

PROJECT_TYPE: "DEFAULT"
# 标识项目类型以进行专门处理

CUSTOM_FOLDER_STRUCTURE: {}
# 项目脚手架的自定义文件夹结构定义

TECHNOLOGY_PRESETS: {}
# 快速选择的预定义技术栈

---

*此文件包含 CursorRIPER Framework 的用户自定义配置。编辑这些设置以调整框架行为以符合您的偏好。* 