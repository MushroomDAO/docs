# Demo — Mycelium 协议如何运作
[English Version](demo-en.md)

> 从零开始，在手机上 2 分钟内创建 Web3 钱包并完成商户积分闭环。

---

## 用户旅程：在本地咖啡馆消费

### 第一步 — 创建 AirAccount（无需助记词）
新用户打开应用，用手机内置的 Passkey（Face ID / 指纹）完成注册。
无密码，无 12 位助记词。账户是一个智能合约钱包（ERC-4337）。

```
用户：[刷脸] → AirAccount 创建完成 → 分配钱包地址
耗时：约 20 秒
```

### 第二步 — 扫码支付
在咖啡馆，用户点击「支付」并扫描商户的二维码。
SuperPaymaster 代付 Gas 费 —— 用户支付 **零 ETH Gas**。

```
用户：扫描二维码 → 确认 ฿85 → 交易发送
Gas：由 SuperPaymaster 赞助（向商户收取 10% 协议费）
链：以太坊 L2（Optimism / Base）
耗时：约 3 秒
```

### 第三步 — 自动铸造积分
Mycelium 协议自动向用户的 AirAccount 铸造社区积分（aPNTs）。
积分可在联盟网络内任意商户兑换，无锁定期，无过期日。

```
用户：收到 85 aPNTs → 余额在应用中可见
商户：看到结算交易 → 积分负债记录上链
```

### 第四步 — 兑换或转赠积分
用户可在任意合作商户兑换积分，赠送给朋友，或质押获得治理权。
无中心化平台控制积分。没有 LINE，没有 Grab，没有中间商。

---

## 基础设施组件

### AirAccount
零摩擦上手的智能合约钱包。

| 功能 | 说明 |
|---|---|
| 认证方式 | Passkey（Face ID / 指纹） |
| 恢复机制 | 通过可信联系人进行社交恢复 |
| 标准 | ERC-4337 账户抽象 |
| Gas | 由 SuperPaymaster 赞助 |
| 仓库 | [github.com/aastarcommunity/AirAccount](https://github.com/aastarcommunity/AirAccount) |

### SuperPaymaster
去中心化 Gas 赞助 —— 商户买单，用户无感。

| 功能 | 说明 |
|---|---|
| 模式 | 商户预存 Gas 预算 |
| 费率 | Gas 费用的 10% 进入协议国库 |
| 无许可 | 任何人均可成为 Paymaster 节点 |
| 仓库 | [github.com/aastarcommunity/SuperPaymaster](https://github.com/aastarcommunity/SuperPaymaster) |

### Sign90
聚合签名安全模块——智能账户核心，支持 Guardian 社交恢复、Session Key 与 EIP-2 高-s 拒绝。

| 功能 | 说明 |
|---|---|
| 标准 | ERC-4337 + BLS 聚合签名 |
| 恢复 | Guardian 多方社交恢复 |
| Session Key | 临时授权，不暴露主密钥 |
| 状态 | M5 完成（Sepolia E2E 验证通过）· M6 Gas 优化进行中 |
| 仓库 | [github.com/aastarcommunity/airaccount-contract](https://github.com/aastarcommunity/airaccount-contract) |

### SDSS（Rain Computing）
驱动链下 AI 与数据层的去中心化计算和存储网络。

[github.com/aastarcommunity/SDSS](https://github.com/aastarcommunity/SDSS)

### CometENS
兼容 ENS 的名称解析服务，适用于 Mycelium 生态系统。

[github.com/aastarcommunity/CometENS](https://github.com/aastarcommunity/CometENS)

### HexagonWarrior
面向社区建设者和节点运营者的桌面客户端。

[github.com/AAStarCommunity/HexagonWarrior-Tauri](https://github.com/AAStarCommunity/HexagonWarrior-Tauri)

---

## 框架

### COS72
DAO 与社区工具框架 —— 在 Mycelium 协议上启动社区的核心骨架。

[github.com/MushroomDAO/COS72](https://github.com/MushroomDAO/COS72)

### Arcadia — Play2B2E 忠诚度系统
游戏化链上积分系统。商户发行积分，用户参与赚取，积分可在网络内交易。

- [Arcadia GitHub](https://github.com/CMUBA/ArcadiaV2)
- [Arcadia 官网](https://arcadia.cmuba.org/)

### Doris 协议
创作者经济协议 —— 内容价值流通与归属确权。

[github.com/MushroomDAO/Doris](https://github.com/MushroomDAO/Doris)

---

## 应用与项目

### Zu.Coffee
诞生于 Zuzalu 的社区实验 —— 在真实咖啡馆验证微循环经济模型。

- [Zu.Coffee GitHub](https://github.com/MushroomDAO/zu.coffee)
- [Zu.Coffee 官网](https://zu.coffee/)

### Chiang Mai Connect
清迈社区的本地信息发现协议 —— 活动、商户、协作。

[github.com/CMUBA/ChiangMaiConnect](https://github.com/CMUBA/ChiangMaiConnect)

---

## 开发进度

*实时同步自 [mushroom.cv](https://www.mushroom.cv/) 看板。最后更新：2026-03-17。*

| 组件 | 任务 | 进度 | 状态 |
|---|---|:---:|---|
| Sign90 智能账户核心 | TASK-10 | **85%** | M5 完成 · M6 Gas 优化启动 |
| SuperPaymaster 论文（AOA/ERC-4337） | TASK-31 | **90%** | BRA Cover Letter + BibTeX 完成，待投稿 |
| CommunityFi 论文（声誉信用） | TASK-32 | **85%** | JBBA citations 更新，投稿包就绪 |
| AirAccount 隐形账户 | TASK-12 | **70%** | v0.16.7 TX 历史统计 · 下一步 Chrome 插件集成 |
| SuperPaymaster 合约 | TASK-4 | **40%** | UUPS v4.0.0 Sepolia 部署 · 信用系统待开发 |
| Phase 1 创世启动（Meta） | TASK-23 | **50%** | MyShop 完成 · GToken 启动待进行 |
| AuraAI 课程 | TASK-35 | **35%** | 5 门课程框架建立 |
| Cos72 核心模块 | TASK-13 | **10%** | MyTask / MyShop / MyVote — Phase 2 目标 |
| Spores SDK | TASK-19 | **5%** | 设计阶段 |

→ [查看完整实时看板 ↗](https://www.mushroom.cv/)

---

## 立即体验

| 资源 | 链接 |
|---|---|
| AAStar 社区（基础设施建设者） | [aastar.io](https://aastar.io) |
| MushroomDAO GitHub | [github.com/MushroomDAO](https://github.com/mushroomdao) |
| 社区 | [Telegram](https://t.me/aastarcommunity) · [Twitter](https://x.com/aastarcommunity) |
| 治理论坛 | gov.mushroom.box *(第二阶段上线)* |
