# prd-to-dev-spec

PRD → 开发就绪规格与开工门禁的生成技能（Agent Skills 规范）。

输入已确认的 PRD（可选叠加原型、代码库、接口契约文档），对每个页面、状态、用户操作执行工程事实核对。事实齐则放行，事实缺则停在缺口报告。不新增产品规则、不定义 API 结构、不编造实现事实。

## 核心能力

- **双态文档**：缺口报告态（阻塞）→ 可开发态（放行），同一文档原地升级
- **12 维度框架**：必查 8 + 触发 4，逐页面逐操作过维度，系统性覆盖工程事实
- **六项门禁**：G1 上游就绪 → G6 边界纯净，每项写明检查内容与证据要求
- **缺口双分**：T-XXX（契约缺口，缺工程合同）+ R-XXX（规则回流项，PRD 本身缺失需回改）
- **重检协议**：影响范围登记 + 结论带版本 + 门禁只认当下
- **预检模式**：无代码库时可作 PRD 体检用，提前暴露工程缺口

## 安装

### Trae

```bash
git clone git@github.com:516249227-crypto/prd-to-dev-spec.git ~/.trae-cn/skills/prd-to-dev-spec
```

或下载 zip 解压到 `~/.trae-cn/skills/` 下。新开对话后说"PRD 转开发就绪规格"即可触发。

### Claude Code

```bash
git clone git@github.com:516249227-crypto/prd-to-dev-spec.git ~/.claude/skills/prd-to-dev-spec
```

### Codex

```bash
git clone git@github.com:516249227-crypto/prd-to-dev-spec.git ~/.agents/skills/prd-to-dev-spec
```

`~/.agents/skills/` 是 Codex、Copilot CLI、Gemini CLI 共同识别的跨运行时目录。

### Gemini CLI

同 Codex，使用 `~/.agents/skills/` 目录。

### 通用（下载 zip）

下载 [releases](https://github.com/516249227-crypto/prd-to-dev-spec/releases) 中的 zip，解压到对应运行时的 skills 目录即可。

## 更新

在技能目录内执行 `git pull`。

## 与 proto-to-prd 配合使用

```
原型 → [proto-to-prd] → PRD → [prd-to-dev-spec] → 开发就绪规格 → 接口契约
```

`proto-to-prd` 负责"用户能看到什么"，`prd-to-dev-spec` 负责"能不能开工"。两个技能形成完整的交付链路。
