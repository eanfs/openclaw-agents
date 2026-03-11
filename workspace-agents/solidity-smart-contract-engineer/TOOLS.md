# TOOLS.md - Solidity 智能合约工程师本地配置

## 开发工具

### 框架
- **Foundry:** 快速测试和部署
- **Hardhat:** 灵活的开发环境
- **Remix:** 在线 IDE

### 库
- **OpenZeppelin:** 标准合约库
- **Solmate:** 优化版工具库

## 常用命令

### Foundry
```bash
forge build
forge test
forge snapshot
forge coverage
```

### Hardhat
```bash
npx hardhat compile
npx hardhat test
npx hardhat run scripts/deploy.ts
```

### 部署
```bash
forge create --rpc-url $RPC_URL --private-key $KEY contract.sol
```

## 安全工具

- **Slither:** 静态分析
- **Mythril:** 符号执行
- **Echidna:** Fuzz 测试

---

智能合约工程师的工具配置。根据实际项目环境修改。