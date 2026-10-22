# Campus-Hanfu-Rental-System
高校汉服租聘管理系统 | 汉服租聘平台  java毕设项目   汉服租赁与科普系统基于SpringBoot3+Vue3开发，采用UserCF协同过滤做个性化推荐，接入星火大模型实现AI智能穿搭建议生成，依托用户身材档案自动尺码匹配；集成WebSocket实时消息，打通汉服百科、租赁交易、UGC穿搭社区全流程，支持学生用户和管理员双端，具备实名认证、订单管控、内容审核等功能。

# 高校汉服租赁平台 · 功能  

## 创新亮点

- 👗 **基于用户收藏的协同过滤推荐**：首页热门推荐采用 UserCF 算法，根据收藏行为个性化推荐汉服，冷启动回退热门商品。
- 📏 **尺码助手 + 智能搭配生成器**：根据用户身材档案自动匹配尺码，并调用星火大模型生成个性化搭配建议文案（如“你155cm/46kg，建议宋制褙子搭配百褶裙”）。
- 📚 **汉服百科独立频道**：按朝代/形制分类，富文本详情，关联商品，兼具教育与导购功能。
- 🛒 **租赁全链路闭环**：选日期、实时计价、模拟支付、状态跟踪、逾期罚金、归还评价，流程完整。
- 💬 **WebSocket 实时通知 + 在线沟通**：订单状态变更、公告、互动提醒实时推送，用户可与管理员在线交流。

---

## 技术栈

### 后端技术栈

| 技术 | 说明 |
|------|------|
| Spring Boot 3 | 核心框架 |
| MyBatis-Plus | 持久层框架 |
| MySQL 8.0 | 关系型数据库 |
| JWT | 身份认证 |
| 协同过滤算法 | 基于用户收藏的推荐算法 |

### 前端技术栈

| 技术 | 说明 |
|------|------|
| Vue 3 | 核心框架 |
| Element UI | UI 组件库 |
| Vue Router | 路由管理 |
| Vuex | 状态管理 |
| Axios | HTTP 客户端 |
| ECharts | 图表可视化 |

---

## 📌 关于本项目

所有代码均由本人亲手编写，采用前后端分离架构，每个系统都实现了完整的业务流程。功能亮点覆盖多个维度，适合作为毕业设计的优质参考。

## 🎯 选题指导

- 本文档旨在为计算机专业同学提供毕业设计选题方向，所列出的每一个题目均配有可运行的完整源码。
- 可写java、springboot论文，全手工，手工画图以及知网文献，一个一个找。只负责初稿。200。先写完给你，可以了最后给钱

## 📥 获取方式

- 微信：**cuteisright**（添加时请备注：git）
- 顺手点个 ⭐Star 就是最大的鼓励～

## ⚠️ 重要声明

1. 本系统仅供学习交流，严禁用于任何商业用途。
2. 代码不免费、不开源、不商用。
3. 所有源码均由本人开发，如有需要请通过上述方式联系。
4. 因项目数量较多，文档中未全部罗列，若未找到心仪的选题，欢迎直接咨询，我会尽力为你推荐最合适的方案。成品原创100（更多项目请联系cuteisright）

---

## 一、学生用户端（Web）

### 1. 用户与账号体系

- **注册/登录**：注册时完成实名认证（学信网或证件审核），登录支持学号+密码，JWT 鉴权。
- **个人中心**：资料编辑、身材档案（身高、体重、三围）、我的收藏、我的评价、我的订单入口。

### 2. 发现与内容（内容即商品）

- **首页**：轮播图、分类导航、热门推荐（基于用户收藏的协同过滤算法）、百科卡片。
- **汉服浏览**：支持搜索、多维筛选（朝代、形制、价格等），详情页聚合基础信息 + 形制科普卡片 + 租赁日历。
- **汉服百科**：独立频道，按朝代/形制分类，富文本详情，关联对应商品。
<img width="1231" height="898" alt="image" src="https://github.com/user-attachments/assets/7f3aaddc-acfc-47de-a870-5bc75c196711" />
<img width="946" height="850" alt="image" src="https://github.com/user-attachments/assets/f79edccc-e26f-407d-9e6c-82b23ba4284e" />
<img width="940" height="879" alt="image" src="https://github.com/user-attachments/assets/d031b5b9-4db8-4954-bbb5-89902cc1359b" />

### 3. 租赁交易闭环

- **尺码助手**：根据用户身材档案自动匹配尺码，在下单页/详情页高亮推荐。
- **下单与支付**：选择租赁日期、实时计价、模拟支付。
- **我的订单**：状态跟踪（待付款、待发货、租赁中、待归还、已完成）、取消、申请归还、评价。
<img width="1246" height="874" alt="image" src="https://github.com/user-attachments/assets/8b34c5bf-6795-4be8-828d-fe2bef319975" />

### 4. 穿搭社区（UGC）

- **笔记流**：浏览、点赞、收藏、评论。
- **发布笔记**：支持图文、标签、关联汉服。
- **我的社区**：我发布的、我点赞的、我收藏的笔记。
<img width="1218" height="790" alt="image" src="https://github.com/user-attachments/assets/4b5a7783-87ca-424a-9328-f0b46acec072" />

### 5. 消息中心

- WebSocket 实时通知：订单状态变更、系统公告、互动提醒（点赞/评论/收藏）、百科更新。
<img width="1255" height="859" alt="image" src="https://github.com/user-attachments/assets/20c377c2-52df-4c9c-91c3-d3e62883299d" />

### 6. 智能搭配与尺码解释生成器

- 在下单页/详情页，调用星火大模型根据用户身材档案 + 汉服形制知识，生成个性化搭配建议文案（如：“根据你155cm/46kg的身材档案，这款宋制褙子属于宽松版型，建议搭配百褶裙，整体显瘦显高……”），并推荐穿搭（从数据库获取，显示对应信息）。
<img width="1261" height="798" alt="image" src="https://github.com/user-attachments/assets/a646b6d5-9dbf-4246-a612-b98ac586ce89" />

### 7. 在线沟通

- 用户可与管理员进行实时对话交流（WebSocket 私聊）。
<img width="1885" height="874" alt="image" src="https://github.com/user-attachments/assets/2418cd27-7b48-4b5c-a5b2-1c52da34ce62" />

---

## 二、平台管理员端（PC 后台）

### 1. 仪表盘

- **核心指标**：订单量、用户数、营收。
- **可视化图表**：ECharts 趋势图、分布图。
- **实时提醒**：新订单、新举报。
<img width="922" height="886" alt="image" src="https://github.com/user-attachments/assets/86d9412a-0d68-4441-8f76-789bb6204f45" />

### 2. 用户与权限

- **用户管理**：列表、搜索、禁用/启用。
- **实名审核**：学信网或证件审核。
- **身材档案查看**：辅助尺码异常排查。
<img width="1843" height="874" alt="image" src="https://github.com/user-attachments/assets/903d5bd8-9813-479e-9927-d1de581cb90a" />

### 3. 商品与内容管理

- **汉服管理**：CRUD、上下架、库存、绑定形制/百科/搭配。
- **分类管理**：朝代、款式、形制维度。
- **百科管理**：条目 CRUD、纠错审核、首页科普编排。
- **轮播图管理**：首页配置，支持跳转商品/百科/笔记。
<img width="1881" height="835" alt="image" src="https://github.com/user-attachments/assets/aeb7c14e-493d-4a07-8553-08510622ce75" />
<img width="1873" height="891" alt="image" src="https://github.com/user-attachments/assets/48f10625-db4e-43f0-9aa2-4d639a662e5c" />

### 4. 交易与运营

- **订单管理**：列表、确认发货/归还、逾期罚金、日历视图。
- **评价管理**：审核、违规删除。
<img width="1852" height="858" alt="image" src="https://github.com/user-attachments/assets/4ed8192c-434a-48dc-8d57-3fdbd24cfdb6" />

### 5. 社区治理

- **笔记审核**：置顶、下架。
<img width="1869" height="886" alt="image" src="https://github.com/user-attachments/assets/0274f7cf-5b09-401e-bdc7-44770b25709f" />
<img width="1885" height="883" alt="image" src="https://github.com/user-attachments/assets/df963e1c-3916-46af-bf93-cd53c0d74da0" />
