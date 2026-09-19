# idealjs/skills

> idealjs 的 AI skill 集合。每个 skill 一个目录，放进你的 Agent 即可用。

这里的 skill 都生长自真实的人机对话：方法先在对话中磨成形，再蒸馏成给 AI 的 SKILL 和给人的 blog。

## code-tree

AI 生成的代码能跑，但没人能读懂：没有以树的形式规划，代码就按最短路径长成图——函数交叉调用，数据交叉引用。

code-tree 让 AI 在生成、重构、审查代码时先规划树形结构。规则只有三条：

- 主干起引导作用，能一口气读完
- 叶子平铺总览，不超过 300 行
- 叶子超载，升级为侧枝，并新配一个主干

规划之后，人的 review 从"逐文件考古"降为"核对一棵树"。

- SKILL 本体：[skills/code-tree/SKILL.md](skills/code-tree/SKILL.md)
- 来龙去脉：《代码是树，不是藤》（[skills/code-tree/references/blog.md](skills/code-tree/references/blog.md)）

## distill

把一段对话蒸馏成两份产出：skill 给未来的 AI，是操作指引；blog 给未来的人，是来龙去脉。

AI 交互式梳理你的叙述，经你认同后落笔；不认同，就继续磨。

- SKILL 本体：[skills/distill/SKILL.md](skills/distill/SKILL.md)
- 写作准则：[skills/distill/references/blog-style.md](skills/distill/references/blog-style.md)

## 安装

把仓库地址和你想要的 skill 告诉你的 Agent，它会自行安装：

> 请从 https://github.com/idealjs/skills 安装 code-tree 和 distill

装好后新开一个会话，输入 `/` 即可看到。SKILL.md 格式与 Claude Code 兼容，放进 `~/.claude/skills/` 同样生效。

## License

[CC BY-NC 4.0](LICENSE) — 禁止商用；分发或包装须署名 idealjs 并附仓库链接。
