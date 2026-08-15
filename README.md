# 陈德金｜AI应用开发工程师

专注于RAG、Agent与Python工程实践，关注检索效果、可控执行、模型成本、链路延迟和可验证交付。

2026届数据科学与大数据技术本科，现居成都。当前持续完善面向企业场景的知识库问答与智能工作流项目。

> 求职方向：AI应用开发、Python后端（AI方向），可立即到岗。

## 代表项目

### [MailPilot｜企业邮件与日程协同Agent](https://github.com/dejin-chen/mailpilot)

- 基于LangGraph与MCP构建邮件分类、回复草拟和会议协调工作流，支持人工审批、Checkpoint恢复、长期记忆、幂等执行与安全审计。
- 在本地固定数据集Benchmark中，108个真实模型分析链样本的平均Token由3992.39降至3153.64，下降21.01%；分析链P95由12.84秒降至10.68秒，下降16.84%。
- 完整HTTP E2E任务结果符合预期率由88.89%提升至97.22%，危险操作审批门禁26/26通过，项目当前自动化测试286项通过。

### [KnowFlow AI｜企业知识库RAG平台](https://github.com/dejin-chen/knowflow-ai)

- 覆盖文档解析切分、Embedding、Chroma与BM25双路召回、加权RRF、结构化LLM Rerank、引用问答、精确答案缓存和离线评测。
- 在单份模拟员工手册的100题锁参测试集上，BM25与向量召回经加权RRF融合并结合LLM Rerank后，将HitRate@3由82%提升至约96%，MRR由0.56提升至约0.91；Rerank异常时自动降级为词法排序。
- 使用缓存键、TTL和索引主动失效控制答案复用边界；命中时跳过Embedding、检索、Rerank与回答模型调用，固定问题集回放中整体Token用量下降11%。

## 技术能力

- **Agent开发：**LangGraph状态编排、Tool Calling、MCP、HITL人工审批、Checkpoint恢复、长期记忆与结构化输出。
- **RAG链路：**文档解析与Chunk切分、Embedding、BM25与向量混合召回、RRF、LLM Rerank、引用溯源、缓存与离线评测。
- **Python工程：**Python、FastAPI、Pydantic、PostgreSQL、Redis、pytest、Docker Compose与GitHub Actions。
- **评测与调试：**Token、平均延迟、P95、工具成功率、HitRate@K、MRR、固定数据集A/B与回归测试。

## 工程取向

- 用固定数据集、基线和测试报告说明优化结果，不把目标数据写成实测数据。
- 为模型输出、工具调用和外部副作用设置结构化约束、降级路径与审计边界。
- README中的指标均来自本地可复现测试，不代表生产环境SLA。
