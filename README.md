# 2026-10 Skills

2026 年 10 月整理的 Agent Skills 合集，含自制技能与朋友提供的技能，共 **41 个技能**（纸火写作套件含 8 个子技能，计为 1 个）和 **9 份参考材料**。重复版本已于 2026-10-25 清理。

A collection of Agent Skills compiled in October 2026, including my own and ones shared by friends: **41 skills** (the Paper-Fire writing suite of 8 sub-skills counts as one) plus **9 reference materials**. Duplicate versions were removed on 2026-10-25.

## 文档 · Documents

| 文件 File | 内容 | Contents |
| --- | --- | --- |
| [SKILLS.md](SKILLS.md) | 每个技能的中英文简介与用法，以及非技能材料说明 | Bilingual description and usage for every skill, plus the non-skill materials |
| [REVIEW-2026-10.md](REVIEW-2026-10.md) | 去重记录、价值排名、产品建议与上线前风险 | De-duplication record, value ranking, product ideas and pre-launch risks |

## 安装 · Installation

每个 ZIP 解压后，包含 `SKILL.md` 的那个文件夹就是一个技能。

Each ZIP unpacks to a folder; the folder that contains `SKILL.md` is the skill.

- **Claude Code**：把技能文件夹放进 `~/.claude/skills/`（个人）或项目内 `.claude/skills/`。 Put the skill folder in `~/.claude/skills/` (personal) or `.claude/skills/` in a project.
- **Claude 应用 / Claude app**：在设置中上传技能 ZIP。 Upload the skill ZIP in settings.
- **Codex 等其他 Agent / Other agents**：放到该 Agent 的技能目录，或直接把 `SKILL.md` 内容作为指令提供。 Place it in that agent's skills directory, or supply `SKILL.md` as instructions.

安装第三方技能前，建议先用本仓库的 `skill-sentinel` 做一次离线安全审计。 Before installing third-party skills, run an offline audit with `skill-sentinel` from this repo.

## 技能索引 · Skill index

### A. 影视导演与视频提示词 · Film directing & video prompts

| 技能 Skill | 文件 File | 简介 | Summary |
| --- | --- | --- | --- |
| arcshot-director | [Arcshot-Director-v1.0.0(5).zip](<Arcshot-Director-v1.0.0(5).zip>) | 通用导演分镜：镜头表、走位、连续性、视频提示词 | General director-storyboarder with prompts and continuity |
| h3-omni-studio | [H3-Omni-Studio-v2.0.0(3).zip](<H3-Omni-Studio-v2.0.0(3).zip>) | MiniMax H3 五模式视频提示词编译器 | Five-mode prompt compiler for MiniMax H3 |
| camera-storyboard-director | [韩剧分镜设计-v2.1.1(2).zip](<韩剧分镜设计-v2.1.1(2).zip>) | 剧本转导演分镜，含韩剧心动专项 | Script-to-storyboard with K-drama romance focus |
| kdrama-performance-director | [韩剧影视演员表演导演-v2.1.0(2).zip](<韩剧影视演员表演导演-v2.1.0(2).zip>) | 表演、潜台词与跨镜情绪接续 | Performance, subtext and emotional continuity |
| idea-to-storyboard | [idea-to-storyboard-v1.0.0(7).zip](<idea-to-storyboard-v1.0.0(7).zip>) | 一句话创意到分镜，导出 HTML 工作台 | One-line idea to storyboard with HTML workbench |
| motion-drama-foundry | [motion-drama-foundry-v1.0.0(5).zip](<motion-drama-foundry-v1.0.0(5).zip>) | 漫剧/AI 视频全流程，单一 Project Ledger | End-to-end motion comic on one Project Ledger |
| libtv-director-suite | [libtv-director-suite-v1.2.0-CLEAN(5).zip](<libtv-director-suite-v1.2.0-CLEAN(5).zip>) | 端到端制作，可经 LibTV 提交生成 | End-to-end production that can submit via LibTV |
| sceneweaver-conductor | [sceneweaver-conductor-1.0.0.zip](<sceneweaver-conductor-1.0.0.zip>) | 按分镜从本地技能库自动调度技能 | Routes each shot to skills from a local library |
| agentic-video-director | [agentic-video-director-v1.0.0(6).zip](<agentic-video-director-v1.0.0(6).zip>) | 编码 Agent 用代码渲染并检查视频 | Coding agents build, render and QC video |
| hitframe-studio | [hitframe-studio-3.0.0(4).zip](<hitframe-studio-3.0.0(4).zip>) | 打斗冲击帧与顿帧/震屏效果 | Impact frames, hitstop and screen shake |
| shortform-retention-director | [shortform-retention-director-v1.0.0-public(2).zip](<shortform-retention-director-v1.0.0-public(2).zip>) | 短视频编导与留存分析 | Short-video scripting and retention analysis |
| zy-cinematic-realism | [zy-cinematic-realism-main(2).zip](<zy-cinematic-realism-main(2).zip>) | 电影感静帧提示词（第三方，CC-BY-NC） | Cinematic still prompts (third-party, CC-BY-NC) |
| interactive-film-ui-fusion | [interactive-film-ui-fusion-v1.1.0(10).zip](<interactive-film-ui-fusion-v1.1.0(10).zip>) | 互动影像 HUD、热区与 QTE | HUD, hotspots and QTEs for interactive film |
| shotpatch-vfx | [ShotPatch_VFX_Public_v2.0.zip](<ShotPatch_VFX_Public_v2.0.zip>) | 实拍视频局部特效增补 | Local VFX added to existing footage |
| ue5-niagara-vfx-forge | [ue5-niagara-vfx-forge-v1.0.0(3).zip](<ue5-niagara-vfx-forge-v1.0.0(3).zip>) | UE5 Niagara 特效施工单与工具 | UE5 Niagara build sheets and tooling |

### B. 剧本与故事 · Screenwriting & story

| 技能 Skill | 文件 File | 简介 | Summary |
| --- | --- | --- | --- |
| microdrama-storyforge | [microdrama-storyforge-v1.1.0(4).zip](<microdrama-storyforge-v1.1.0(4).zip>) | 竖屏微短剧 15 集剧本工厂 | 15-episode vertical micro-drama factory |
| novel-to-episode | [novel-to-episode(3).zip](<novel-to-episode(3).zip>) | 小说改编单集商业短剧 | Novel to one pitch-ready episode |
| screenplay-forge | [Screenplay-Forge-v2.0.0.zip](<Screenplay-Forge-v2.0.0.zip>) | 剧本诊断、评分与重写 | Script diagnosis, scoring and rewrite |
| commercial-feature-screenwriter | [commercial-feature-screenwriter-v1.2.0.zip](<commercial-feature-screenwriter-v1.2.0.zip>) | 商业长片编剧（英文为主） | Commercial feature screenwriting (English-first) |
| echo-street-audio-drama | [echo-street-audio-drama-v1.0.0(3).zip](<echo-street-audio-drama-v1.0.0(3).zip>) | 儿童分龄有声剧 | Age-tiered children's audio drama |

### C. 图像、资产与实体设计 · Image, asset & physical design

| 技能 Skill | 文件 File | 简介 | Summary |
| --- | --- | --- | --- |
| asset-reality-studio | [asset-reality-studio-v3.3.0-clean(3).zip](<asset-reality-studio-v3.3.0-clean(3).zip>) | 真实感影视资产与客户三联模板 | Photoreal film assets and client triptych |
| realm-lock | [realm-lock-v1.0.0(2)(3).zip](<realm-lock-v1.0.0(2)(3).zip>) | 写实资产与跨镜一致性 | Photoreal assets and cross-shot consistency |
| character-clean-extractor | [character-clean-extractor-v2.0.0-public(3).zip](<character-clean-extractor-v2.0.0-public(3).zip>) | 从参考图提取人物身份与服装 | Extract character identity and wardrobe |
| packaging-visual-direction | [Packaging_Visual_Direction_Skill_v1.0.0(3).zip](<Packaging_Visual_Direction_Skill_v1.0.0(3).zip>) | 产品包装排版、配色与风格方向 | Packaging layout, color and style directions |
| printforge-3d-printing | [PrintForge_3D_Printing_Skill_v2.0.0.zip](<PrintForge_3D_Printing_Skill_v2.0.0.zip>) | 图片到可打印 3D 模型 | Images to printable 3D models |
| cat-punch-meme | [穿越平行世界爱因斯坦罗森桥系统skill(3).zip](<穿越平行世界爱因斯坦罗森桥系统skill(3).zip>) | 猫拳表情包生图提示词 | Cat-punch meme prompts |

### D. 文字写作 · Writing

| 技能 Skill | 文件 File | 简介 | Summary |
| --- | --- | --- | --- |
| natural-writer | [爆款文章地表最猛写作系统(3).zip](<爆款文章地表最猛写作系统(3).zip>) | 中文写作七步法与去 AI 腔 | Seven-step Chinese writing and de-AI |
| magic-style-dna | [魔法文风-写作DNA-v2.0.0-外发完整版(2).zip](<魔法文风-写作DNA-v2.0.0-外发完整版(2).zip>) | 作者文风迁移与传播复盘 | Author-style transfer and performance review |
| public-writing-starter | [github-public-writing-starter-v2.0.0(3).zip](<github-public-writing-starter-v2.0.0(3).zip>) | 短内容从选题到成稿 | Short-form writing from topic to draft |
| 纸火写作套件 Paper-Fire suite | [纸火-自由写作实验桌-v3.0.0-外发纯净版(3).zip](<纸火-自由写作实验桌-v3.0.0-外发纯净版(3).zip>) | 8 个单点写作工具 | Eight single-purpose writing tools |

### E. 思考、Agent 工程与工具 · Thinking, agent engineering & utilities

| 技能 Skill | 文件 File | 简介 | Summary |
| --- | --- | --- | --- |
| bedrock-agora | [bedrock-agora-2.0.0.zip](<bedrock-agora-2.0.0.zip>) | 第一性原理决策与 Skill 创作 | First-principles decisions and skill authoring |
| faultline-wargame | [faultline-wargame-1.0.0.zip](<faultline-wargame-1.0.0.zip>) | 计划压力测试与反方推演 | Stress-testing plans and arguments |
| idea-prism | [idea-prism.zip](<idea-prism.zip>) | 从长对话提炼思想卡 | Distill long chats into idea cards |
| vibe-coding-intent-compiler | [vibe-coding-intent-compiler.zip](<vibe-coding-intent-compiler.zip>) | 口语需求编译为执行合同 | Vague requests into an execution contract |
| sharp-dialogue-protocol | [sharp-dialogue-protocol(2).zip](<sharp-dialogue-protocol(2).zip>) | 防漂移对话协议与断点续传 | Anti-drift protocol with checkpoints |
| agent-instruction-optimizer | [agent-instruction-optimizer-v2.0.0.zip](<agent-instruction-optimizer-v2.0.0.zip>) | 优化 system prompt、AGENTS.md 与 Skill | Optimize system prompts, AGENTS.md and skills |
| skill-sentinel | [skill-sentinel-v1.0.0(4).zip](<skill-sentinel-v1.0.0(4).zip>) | Skill 离线安全审计 | Offline security audit for skills |
| library-steward | [library-steward(3).zip](<library-steward(3).zip>) | 本地知识库检索与管理 | Local knowledge-base search and management |
| infinite-canvas-function-architect | [infinite-canvas-function-architect-v1.2.0.zip](<infinite-canvas-function-architect-v1.2.0.zip>) | 需求转可编辑无限画布 | Requirements into an editable infinite canvas |
| codex-clean | [codex-clean-main(3).zip](<codex-clean-main(3).zip>) | 编码 Agent 缓存与日志清理 | Clean coding-agent caches and logs |
| download-anything | [download-anything(4).zip](<download-anything(4).zip>) | 资源查找与下载（第三方） | Find and download resources (third-party) |

## 参考材料 · Reference materials

这些文件不是技能，详见 [SKILLS.md](SKILLS.md#非技能材料--non-skill-materials)。 These are not skills; see SKILLS.md for details.

- [AI-Learning-12-Weeks-v1(1).zip](<AI-Learning-12-Weeks-v1(1).zip>) — 12 周 AI 学习课程 · 12-week AI course
- [Survival_Cast_AssetKit_v1.zip](<Survival_Cast_AssetKit_v1.zip>) — 18 人角色资产包 · 18-character cast kit
- [awesome-opus-5.5-video-main(4).zip](<awesome-opus-5.5-video-main(4).zip>) — Opus 5.5 视频案例清单（第三方） · Video case list (third-party)
- [lordaeron-lastwatch-v1.0(3).zip](<lordaeron-lastwatch-v1.0(3).zip>) — 魔兽同人塔防小游戏 · Warcraft fan tower-defense game
- [skill-control-center-v1.0.0(1)(1).zip](<skill-control-center-v1.0.0(1)(1).zip>) — 技能管理桌面应用界面补丁 · Skill-manager app UI patch
- [映衡｜导演的创作与判断协作协议.md](<映衡｜导演的创作与判断协作协议.md>) — 导演 AI 协作协议 · Director's AI collaboration protocol
- [AI影视创作知识库_搭建方案_v4(2).md](<AI影视创作知识库_搭建方案_v4(2).md>) — 影视知识库搭建方案 · Film knowledge-base build plan
- [韩剧双Skill独立审查报告-2026-10-20(2).md](<韩剧双Skill独立审查报告-2026-10-20(2).md>) — 韩剧双技能审查报告 · K-drama skills audit report
- [Son-of-Seagal.pdf](<Son-of-Seagal.pdf>) — 英文电影剧本，测试素材（他人作品） · English screenplay used as test material (third-party work)

## 许可 · Licensing

各技能遵循其包内声明的许可；第三方与朋友提供的技能，版权归原作者所有。 Each skill follows the license stated in its package; third-party and friend-contributed skills remain the property of their authors.
