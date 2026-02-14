# SOLANA SOR 智能合约

[English](README.md) | 简体中文

## 概述

SOLANA SOR（智能订单路由）智能合约仓库在 Solana 区块链上实现了一个去中心化交易所（DEX）。该项目利用 Solana 程序库（SPL）和 Anchor 框架，提供强大且高效的代币交换功能。

## 仓库结构

- `programs/`: 包含 DEX 的 Solana 智能合约（链上程序）。
  - `src/`:
    - **adapters/**: 提供抽象层，用于将各种外部协议和工具集成到 DEX 中，确保模块化和可扩展的架构。
    - **instructions/**: 包含核心程序逻辑，处理 DEX 的基本功能，如代币交换、流动性管理和费用计算。
    - **utils/**: 包含程序中使用的实用函数和辅助方法。
- `Anchor.toml`: Anchor 项目的配置文件。
- `Cargo.toml`: Rust 项目配置文件。
- `package.json`: 包含基于 JavaScript 的测试或工具的依赖项和脚本。

## 主要功能

- **拆分交易**: DexRouter 支持拆分交易，使用户能够跨多个流动性来源执行交易。
- **安全性**: 合约已通过 OKX 内部审计团队的审计。
- **可扩展架构**: 可轻松与其他基于 Solana 的程序和代币集成。
- **Anchor 框架**: 利用 Anchor 实现无缝的程序开发和部署。
- **高性能**: 基于 Solana 构建，确保高吞吐量和低延迟。

## 前置要求

- **Rust**: 从 [rustup.rs](https://rustup.rs/) 安装 Rust。
- **Solana CLI**: 从 [Solana CLI 文档](https://docs.solana.com/cli/install-solana-cli-tools) 安装 Solana 命令行工具（推荐版本：**1.18.26** 以确保兼容性）。
- **Anchor 框架**: 运行以下命令安装 Anchor：

  ```bash
  cargo install --git https://github.com/coral-xyz/anchor avm --force
  ```

  或者，按照 [Solana 文档](https://solana.com/docs/intro/installation) 中的安装指南进行操作，以确保兼容性和正确设置（推荐版本：**0.30.0** 和 **0.30.1** 以确保兼容性）。
- **Node.js** 和 **npm**（或 **yarn**）用于 JavaScript 工具。

---

## 安装和使用

1. **克隆仓库**:
   ```bash
   git clone https://github.com/okx/WEB3-DEX-SOLANA-OPENSOURCE.git
   cd WEB3-DEX-SOLANA-OPENSOURCE
   ```

2. **安装依赖**:
- 使用 Yarn:
  ```bash
  yarn install
  ```

- 使用 npm:
  ```bash
  npm install
  ```

3. **构建项目**:
   使用 Anchor 构建智能合约：
   ```bash
   anchor build
   ```

4. **部署智能合约**:
   在 `Anchor.toml` 中配置适当的集群 URL 并部署：
   ```bash
   anchor deploy
   ```

5. **运行测试**:
   使用 Anchor 的测试套件确保功能正常：
   ```bash
   anchor test
   ```

---

# 贡献

有几种方式可以为 SOR 智能合约项目做出贡献：

## 贡献方式

### 加入社区讨论
加入我们的 [Discord 社区](https://discord.gg/3N9PHeNn)，帮助其他开发者解决集成问题，并分享您使用 SOR 智能合约的经验。我们的 Discord 是技术讨论、问题和实时支持的主要中心。

### 提交 Issue
- 打开 [issues](https://github.com/okx/WEB3-DEX-SOLANA-OPENSOURCE/issues) 来建议功能或报告小错误
- 在打开新 issue 之前，请搜索现有 issue 以避免重复
- 请求功能时，请包含有关用例和潜在影响的详细信息

### 提交 Pull Request
1. Fork 仓库
2. 创建功能分支
3. 进行更改
4. 运行测试
5. 提交 pull request

### Pull Request 指南
- 首先在 issue 中讨论非琐碎的更改
- 为新功能添加测试
- 根据需要更新文档
- 在 PR 中添加描述您更改的变更日志条目
- PR 应该专注，最好解决单一问题

## 首次贡献者
- 查找标记为 "good first issue" 的 issue
- 阅读我们的文档
- 按照安装指南设置本地开发环境

## 代码审查流程
1. 维护者将审查您的 PR
2. 处理任何请求的更改
3. 一旦获得批准，您的 PR 将被合并

## 有问题？
- 打开讨论 [issue](https://github.com/okx/WEB3-DEX-SOLANA-OPENSOURCE/issues) 询问一般问题
- 加入我们的 [社区](https://discord.gg/3N9PHeNn) 进行实时讨论
- 查看现有的 issue 和讨论

感谢您为 SOLANA SOR 智能合约仓库做出贡献！
