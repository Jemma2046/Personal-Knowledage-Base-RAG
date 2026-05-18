Personal Knowledge Base Built with Dify (RAG‑Based Solution)

English Version

Project Overview

a private RAG‑powered personal knowledge base using Dify and open‑source LLMs, following standard RAG pipeline architecture to centralise materials and documents into a retrievable, accurate knowledge system.
<img width="2097" height="814" alt="image" src="https://github.com/user-attachments/assets/e2d614fd-40ed-4bf3-8380-6f5f68c433cd" />

demo: 
.......

Core Business Value

• Eliminates AI hallucinations by anchoring outputs to verified personal and professional materials.

• Enables instant access to proprietary domain knowledge without repeated manual searching.

• Delivers a low‑code, scalable solution to build internal enterprise knowledge hubs, fully transferable to AXA’s AI learning and enablement scenarios.

RAG‑Driven Implementation Workflow

1. Ingestion: Import unstructured data including PDFs, text notes and internal documents, then split raw content into fine‑grained text chunks and generate vector embeddings.

2. Storage: Store embeddings and original text in a vector database connected via Dify, supporting efficient semantic search and long‑term knowledge accumulation.

3. Retrieval: When querying professional questions, the system automatically searches for context‑matched content from the knowledge base based on semantic similarity.

4. Augmentation & Generation: Inject retrieved relevant chunks into LLM prompts, enabling the model to generate grounded, non‑hallucinatory responses supported by my private data.
   

中文版本

项目概述

我基于 Dify平台结合开源大模型，搭建了一套RAG架构的个人私有知识库，将零散的学习资料、专业文档和笔记等非结构化数据整合为可检索、高精准的知识系统。

核心业务价值

• 依托真实资料锚定AI输出，从根源减少大模型幻觉问题，保证回答严谨合规；

• 实现私有专业知识快速调取，无需重复翻阅资料，大幅提升学习与工作效率；

• 提供低代码、可规模化的企业内部知识库搭建方案，可直接迁移应用于AXA内部AI学习赋能场景。

基于RAG的实现流程

1. 数据摄取（Ingestion）：导入PDF、笔记、文档等非结构化资料，将原始内容切分为文本片段，生成向量嵌入（embeddings）。

2. 向量存储（Storage）：通过Dify对接向量数据库，保存向量数据与原文，实现语义级检索与知识长期沉淀。

3. 智能检索（Retrieval）：当查询专业问题时，系统根据语义相似度，从知识库中匹配并调取最相关的内容片段。

4. 增强生成（Augmentation & Generation）：将检索到的上下文注入大模型提示词，让AI基于私有资料生成有依据、无幻觉的精准回答。






# Dify 知识库使用指南
基于 Dify 构建的智能知识库，支持文档上传、自动解析、语义检索、智能问答，可快速对接业务场景，实现知识高效管理与问答赋能。


## 一、项目简介
本项目依托 **Dify 平台**搭建个人专属知识库，通过上传结构化/非结构化文档（PDF/Word/Excel/Markdown 等），自动完成文本切片、向量化存储，结合大语言模型实现**精准语义检索、智能问答**，无需复杂开发即可快速落地应用。

## 二、核心功能
- 支持多格式文档批量上传与自动解析
- 自定义文本切片规则、检索召回策略
- 精准语义检索，返回关联知识片段
- 智能问答：基于知识库内容精准回答，拒绝幻觉
- 实时文档更新、知识校验与管理

## 三、环境准备(refer to setup guide)
1. 部署/访问 Dify 平台
   - 在线版：直接使用 [Dify 官方平台](https://dify.ai/)
   - 私有化部署：参考 [Dify 部署文档](https://docs.dify.ai/)
2. 配置大模型（通义千问/文心一言/GLM/OpenAI 等）
3. 准备待导入的知识库文档

## 四、快速使用步骤
### 1. 创建知识库
1. 登录 Dify 控制台 → 进入「知识库」模块
2. 点击「创建知识库」，选择索引类型（常规/专属）
3. 填写知识库名称、描述，选择嵌入模型

### 2. 上传文档
1. 进入创建好的知识库 → 点击「上传文档」
2. 选择本地文件/批量导入，支持拖拽上传
3. 配置切片规则（分段大小、分隔符）
4. 启动解析与向量化，等待完成

### 3. 检索与测试
1. 在知识库「检索测试」输入问题
2. 查看召回的知识片段，验证准确性
3. 调整切片/检索参数优化效果

### 4. 创建应用（智能问答）
1. 返回控制台 → 创建「对话应用」
2. 关联已创建的知识库，配置prompt
3. 调试对话模型、温度、上下文等参数
4. 发布应用，获取访问链接/API

## 五、API 对接（可选）
Dify 提供标准化 API，可快速集成到外部系统：
- 对话接口：`/v1/chat-messages`
- 检索接口：`/v1/datasets/{dataset_id}/retrieve`
- 文档管理接口：支持上传、删除、查询文档

详细 API 文档：[Dify API 参考](https://docs.dify.ai/development/openapi)

## 六、最佳实践
1. 文档预处理：去除冗余内容，统一格式，提升检索精度
2. 切片规则：短文本用小分段，长文档用大分段+语义分段
3. 检索优化：优先使用「高精度检索」，结合重排序模型
4. 定期更新：及时同步最新业务知识，保证问答时效性

## 七、常见问题
1. **文档解析失败**：检查文件格式、大小，修复损坏文件后重试
2. **检索结果不准确**：优化切片规则、补充关键词、更换嵌入模型
3. **回答偏离知识库**：开启「严格依赖知识库」，优化prompt
4. **API 调用失败**：检查 API Key、权限、请求参数

---
