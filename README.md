# idealjs/skills

> idealjs 组织的 AI 编码 SKILL 集合。每个 skill 一个目录,装进你的 Agent 即可用。

## SKILL 一览

### code-tree

组织必须是树:主干/侧枝/叶子递归同构,叶子 ≤ 300 行,反模式是藤、碎片、超载。让 AI 在生成、重构、审查代码时主动规划树形结构。

- SKILL 本体:[skills/code-tree/SKILL.md](skills/code-tree/SKILL.md)
- 来龙去脉:《代码是树,不是藤》,[skills/code-tree/references/blog.md](skills/code-tree/references/blog.md)

### distill

把一段对话蒸馏成 skill + AI 视角的 blog:交互式梳理问题,经用户认同后,产出给 AI 的操作指引和给人类的来龙去脉记录。

- SKILL 本体:[skills/distill/SKILL.md](skills/distill/SKILL.md)
- blog 写作准则:[skills/distill/references/blog-style.md](skills/distill/references/blog-style.md)

## 安装教程

### 用户级安装(推荐,对所有项目生效)

```bash
git clone https://github.com/idealjs/skills.git
cd skills

mkdir -p ~/.agents/skills
cp -r skills/code-tree skills/distill ~/.agents/skills/
```

只装其中一个,把 `cp` 的路径换成对应的即可。

### 项目级安装(只对当前项目生效)

```bash
git clone https://github.com/idealjs/skills.git /tmp/skills
mkdir -p .agents/skills
cp -r /tmp/skills/skills/code-tree /tmp/skills/skills/distill .agents/skills/
rm -rf /tmp/skills
```

### 符号链接(跟随仓库更新)

```bash
git clone https://github.com/idealjs/skills.git ~/skills
mkdir -p ~/.agents/skills
ln -s ~/skills/skills/code-tree ~/.agents/skills/code-tree
ln -s ~/skills/skills/distill ~/.agents/skills/distill
```

### 验证安装

重启 ZCode(或新开一个会话),输入 `/` 查看可用 skills。SKILL.md 格式与 Claude Code 兼容,复制到 `~/.claude/skills/` 即可。

## 目录结构

```text
skills/
├── README.md
├── LICENSE                          # CC BY-NC 4.0
└── skills/
    ├── code-tree/
    │   ├── SKILL.md
    │   └── references/
    │       └── blog.md              # 《代码是树,不是藤》
    └── distill/
        ├── SKILL.md
        └── references/
            └── blog-style.md        # blog 写作准则
```

## License

[CC BY-NC 4.0](LICENSE) — 禁止商用;分发或包装须署名 idealjs 并附仓库链接。
