# 技能说明与用法 · Skill Guide

本仓库全部技能的中英文简介与用法。引号中的句子是可以直接对 AI 说的触发语。安装方法与文件索引见 [README](README.md)，排名与产品建议见 [REVIEW-2026-10.md](REVIEW-2026-10.md)。

Bilingual description and usage for every skill in this repo. Quoted lines are prompts you can say as-is. See the [README](README.md) for installation and the file index, and [REVIEW-2026-10.md](REVIEW-2026-10.md) for rankings and product ideas.

## A. 影视导演与视频提示词 · Film directing & video prompts

**arcshot-director · 导演分镜师**

- 简介：通用导演与分镜师。把创意、剧本、广告或动作场面变成镜头表、空间走位、连续性账本、AI 视频提示词与声音剪辑方案，分快捷/分镜/项目/修复四种深度。
- Description: A general director-storyboarder. Turns ideas, scripts, ads or action scenes into shot lists, blocking, a continuity ledger, AI video prompts and sound/edit plans, at quick, storyboard, project or repair depth.
- 用法：“把这段剧本做成分镜和视频提示词”；“生成的第 3 镜人物变脸了，怎么修”。
- Usage: “Turn this scene into a storyboard with video prompts.” / “Shot 3 changed the actor's face — fix it.”

**h3-omni-studio · H3 全模式视频提示词**

- 简介：面向 MiniMax H3 的提示词编译器，按素材用途自动选择 T2VA/I2VA/FL2VA/L2VA/Ref2VA 五种模式之一，输出可直接粘贴的字段化提示词，含对白配音、动作物理与单点修复。只写提示词，不调用付费 API。
- Description: A prompt compiler for MiniMax H3. Picks exactly one of five modes from what your reference media is for, and outputs paste-ready field-structured prompts, including dialogue, physics and targeted repair. Writes prompts only; no paid API calls.
- 用法：“用 H3 Omni 写一条 8 秒写实视频：……”；附首帧图时说明“这张是第 0 秒画面”。
- Usage: “Write an 8-second realistic H3 prompt: …” Attach a first frame and say “this is frame 0” to get I2VA.

**camera-storyboard-director v2.1.1 · 韩剧分镜设计**

- 简介：把剧本转成可拍的导演分镜：调度、构图、视点、运镜、焦点、升格与剪辑。内置青春心动、暧昧拉扯、成熟关系专项。只出分镜，每个新项目必须给画幅。
- Description: Turns scripts into shootable director's storyboards covering blocking, composition, POV, camera moves, focus, slow motion and cuts, with K-drama romance specialties. Storyboards only; every new project must state an aspect ratio.
- 用法：“画幅 9:16，把下面片段做成青春心动分镜，要一次有理由的慢动作”。
- Usage: “9:16. Make this a first-crush storyboard with one motivated slow-motion beat.”

**kdrama-performance-director · 韩剧表演导演**

- 简介：为韩剧取向场景设计人物行动、潜台词、微表情与跨镜情绪接续，可适配已有分镜，修正“太用力、没交流感、情绪断了”。与上一个技能成对使用。
- Description: Designs actions, subtext, micro-expressions and emotional continuity across shots for K-drama-style scenes; adapts to an existing storyboard and fixes over-acting or missing connection. Pairs with the storyboard skill above.
- 用法：“分镜已定，只改表演，让两人真正接住对方的反应”。
- Usage: “Storyboard is locked; change performance only so they actually react to each other.”

**idea-to-storyboard · 故事分镜构建师**

- 简介：从一句话创意写出有因果的完整故事与镜头表，用内置 Python 校验后导出可离线打开的 HTML 分镜工作台、CSV 与 Markdown。
- Description: Grows a one-line idea into a causal story and shot list, validates it with bundled Python, and exports an offline HTML storyboard workbench, CSV and Markdown.
- 用法：“把这个点子做成 60 秒短片分镜并导出 HTML”（需要能跑 Python 的 Agent，如 Claude Code）。
- Usage: “Make this idea a 60-second short storyboard and export the HTML” (needs an agent that can run Python).

**motion-drama-foundry · 漫剧一体化生产**

- 简介：从一句故事、已有剧本或素材出发，统一完成剧本、人物/场景/道具资产、分镜、连续性、视频提示词与声音交接。全程只认一份 Project Ledger，可中途接管或只修责任层。
- Description: End-to-end motion-comic/AI-video production from story to script, assets, storyboard, continuity, prompts and sound handoff, all on one Project Ledger. Can take over mid-project or repair only the failing layer.
- 用法：“从这个故事开始，一路做到视频提示词”；“接管我的剧本，从资产设定开始”。
- Usage: “Take this story all the way to video prompts.” / “Take over my script from asset design onward.”

**libtv-director-suite · LibTV 导演制作套件**

- 简介：端到端 AI 视频制作：节拍图、资产锁定、调度、分镜、生成计划、连续性与交付。可通过 LibTV 插件或 CLI 真正提交生成，付费生成前必须征得同意。
- Description: End-to-end AI video production that can actually submit jobs through the LibTV plugin or CLI, with mandatory approval before any paid generation. Four modes: director, delegate, hybrid, legacy-read.
- 用法：“用 director 模式先出制作计划，不花钱”；确认后“用 hybrid 模式生成第 1–3 镜”。
- Usage: “Director mode: production plan only, no spend.” Then “Hybrid mode: generate shots 1–3.”

**sceneweaver-conductor · 影视技能总调度**

- 简介：把剧本拆成分镜后，从你本地的技能库（含 ZIP）自动检索匹配的技能（如冲击帧、对白），按段套用并生成逐镜提示词与技能来源记录。
- Description: Breaks a screenplay into shots, searches your local skill library (folders and ZIPs) for the right skill per segment, applies it, and produces per-shot prompts with a record of which skill was used.
- 用法：`python scripts/conductor.py build --script 剧本.md --root 技能文件夹 --out 产物目录`。你这个仓库本身就可作为它的技能库。
- Usage: Run the `conductor.py build` command above; this very repo can serve as its skill library.

**agentic-video-director · Agent 视频导演**

- 简介：给 Claude Code / Codex 用的视频制作技能。把视频当成可构建的工程产物：锁定镜头合同、写代码渲染（如 Remotion/ffmpeg）、检查真实画面与音频、修复后交付文件。
- Description: For coding agents. Treats video as a build artifact: lock a shot contract, implement and render in code, inspect real frames and audio, repair defects, deliver the actual file.
- 用法：在 Claude Code 中说“给我的产品做一条 30 秒发布视频，用这些截图和音乐”。
- Usage: In Claude Code: “Make a 30-second launch video from these screenshots and this track.”

**hitframe-studio · 击帧导演**

- 简介：专做打斗“关键一击”：冲击帧生图/生视频提示词、连招多镜衔接、参考图拆解，以及给现成视频按帧加顿帧、闪白、震屏等效果。支持 Midjourney、即梦、Seedance、可灵、Veo 等。
- Description: Designs the decisive hit in fight scenes: impact-frame image and video prompts, combo continuity, reference breakdowns, plus frame-accurate hitstop, flash and screen-shake on existing footage. Covers Midjourney, Seedance, Kling, Veo and more.
- 用法：“做一张漫剧风斩击冲击帧，用即梦”；“给这段视频第 2.4 秒加顿帧和闪白”。
- Usage: “A manga-style slash impact frame for Seedream.” / “Add hitstop and a white flash at 2.4 s.”

**shortform-retention-director · 短视频编导与留存**

- 简介：把选题或素材变成可拍可剪的短视频方案：真实承诺的钩子、逐秒脚本、字幕声音、平台适配，并用脚本分析发布后的留存曲线。不把模拟评分当真实留存。
- Description: Turns a topic or raw footage into a shootable short with an honest hook, second-by-second script, captions and sound, platform fit, and post-launch retention analysis via script. Never passes simulated scores off as real retention.
- 用法：“做一条 45 秒抖音知识类脚本：……”；“这是我上条视频的留存数据，告诉我观众在哪里走了”。
- Usage: “A 45-second Douyin explainer script about …” / “Here's my retention data — where did viewers drop?”

**zy-cinematic-realism · 造梦师（第三方）**

- 简介：把简短场景想法变成克制、可信的电影感静帧/关键帧英文提示词，先建故事节点、空间和动机光再加镜头术语。作者 popopo-99，许可 CC-BY-NC-4.0（禁止商用）。
- Description: Turns brief ideas into restrained, believable cinematic still/keyframe prompts in English, building story beat, space and motivated light before lens jargon. By popopo-99 under CC-BY-NC-4.0 (no commercial use).
- 用法：“雨夜便利店门口，女人等一个不会来的人，给我电影感提示词”。
- Usage: “A woman outside a convenience store on a rainy night, waiting for someone who won't come — cinematic prompt.”

**interactive-film-ui-fusion · 互动影像 UI 融合**

- 简介：为互动电影/FMV/H5 分支视频设计 HUD、热区、QTE、交互反馈与跟随视频的叠加层，生成审阅用分镜 HTML，并导出 Web/Remotion/Unity 适配。
- Description: Designs the interaction layer for interactive films, FMV and branching H5 video: HUD, hotspots, QTEs, feedback and video-tracked overlays, with a review storyboard HTML and Web/Remotion/Unity adapters.
- 用法：`python scripts/build_project.py project.json build --clean`，先看 `storyboard.html`。
- Usage: Run the build script above, then review `storyboard.html` first.

**shotpatch-vfx · 实拍局部特效增补**

- 简介：给已有实拍视频局部加火、烟、弓箭、手持道具或魔法光效，不动人物和场景。含离线体检、简易跟踪、遮挡合成、ROI 变更审计与 GUI；云端模型只给操作卡。
- Description: Adds localized effects (fire, smoke, arrows, props, magic light) to existing live footage without altering people or sets. Offline inspection, simple tracking, occlusion compositing, ROI change audit and a GUI; cloud models get operation cards only.
- 用法：上传视频并说“别改人，只给屋顶加火”。
- Usage: Upload footage: “Don't touch the actors, just set the roof on fire.”

**ue5-niagara-vfx-forge · UE5 Niagara 特效施工**

- 简介：把自然语言特效需求变成 Niagara 分层施工单、User 参数契约、蓝图触发、性能预算与 QA 表；带 10 种特效 JSON 预设和 Unreal Editor Python 安全复制工具。
- Description: Turns VFX requests into layered Niagara build sheets, user-parameter contracts, Blueprint triggers, performance budgets and QA; ships 10 JSON presets and a safe Unreal Editor Python template-copy tool.
- 用法：“给我的 UE5.5 项目做一个蓝色闪电剑气技能特效，移动端预算”。
- Usage: “A blue lightning sword-slash skill VFX for my UE5.5 project, mobile budget.”

## B. 剧本与故事 · Screenwriting & story

**microdrama-storyforge v1.1 · 13 职能微短剧剧本工厂**

- 简介：把生活素材或原创创意开发成抖音/红果竖屏微短剧：题材重构、15 集大纲、第一集强钩子、逐集写作、反转、拍摄成本与合规检查。带项目 CLI，可存档续写、做影响分析。
- Description: Develops vertical micro-dramas for Douyin/Hongguo: concept rework, 15-episode outline, a hooked episode 1, episode-by-episode drafting, twists, budget and compliance checks. A project CLI saves progress and traces the impact of changes.
- 用法：“把这个婆媳矛盾的真实故事改成 15 集微短剧，先给大纲和第一集”；“从上次的 checkpoint 继续写第 6 集”。
- Usage: “Turn this real in-law conflict into a 15-episode micro-drama; outline and episode 1 first.” / “Resume from the checkpoint and write episode 6.”

**novel-to-episode · 小说改单集短剧**

- 简介：把几万到几十万字小说改成一集 1000–2000 字、开场 3 行内即冲突的商业短剧剧本。内置“改编主笔 / 甲方 / 红队去 AI 味”三角色与 `ai_check.py` 评分。
- Description: Adapts a novel of tens to hundreds of thousands of characters into one 1,000–2,000-character pitch episode with conflict in the first 3 lines. Three internal roles (writer, client, anti-AI red team) plus an `ai_check.py` score.
- 用法：上传小说全文或梳概：“改成一集能拿给甲方的样片剧本”。
- Usage: Upload the novel or synopsis: “Make one pitch-ready sample episode for the client.”

**screenplay-forge · 剧本深度改造**

- 简介：对已有剧本做证据化诊断、十一维评分、反套路审查、分级重写与前后对照。默认交完整新稿，而非只给建议；也能诊断反复生成失败的 AI 视频剧本。
- Description: Evidence-based script doctoring: 11-dimension scoring, anti-cliché review, tiered rewrites and before/after comparison. Delivers a full revised draft by default; also diagnoses scripts that keep failing in AI video.
- 用法：“给这个剧本打分并指出最大的问题”（只评价）；“按中度改写出一版新稿”（实际产出稿件）。
- Usage: “Score this script and name the biggest problem” (review only) / “Do a medium-depth rewrite” (full new draft).

**commercial-feature-screenwriter · 商业长片编剧**

- 简介：英文为主的商业长片编剧技能，9 种模式覆盖概念、结构拆解（45–60 场）、大纲、写场、对白、审稿、删减与 AI 可制作性。先保故事，再考虑 AI 生产。
- Description: English-first feature screenwriting with 9 modes: concept, break (45–60 scenes), treatment, scene, dialogue, review, cut, AI-producibility and full. Story comes first; AI production constraints apply only on a second pass.
- 用法：“BREAK mode: build the sequence map for this premise”；“REVIEW mode on my draft”。
- Usage: Name a mode: “BREAK this premise”, “REVIEW my draft”, “CUT 15 minutes”.

**echo-street-audio-drama · 儿童有声剧**

- 简介：为喜马拉雅等儿童音频平台原创分龄连续有声剧：反套路剧情、价值观自然呈现、对白、音效/配乐/停顿设计与专辑策划。默认 7–10 岁、10 集、每集 8–10 分钟。
- Description: Original age-tiered serialized audio dramas for kids' platforms like Ximalaya: anti-formula plots, values shown through action, dialogue, sound and pause design, album planning. Default 7–10 years, 10 episodes of 8–10 minutes.
- 用法：“做一部 6–8 岁睡前模式的科幻有声剧，先给专辑策划和第一集”。
- Usage: “A bedtime-mode sci-fi audio drama for ages 6–8: album plan and episode 1.”

## C. 图像、资产与实体设计 · Image, asset & physical design

**asset-reality-studio v3.3 · 真实感资产工作室**

- 简介：制作、诊断、修复必须像真实拍摄的影视资产：人物身份/服装板、场景、道具、状态变体，去掉塑料皮肤。内置客户固定三联模板（2100×1172，左正面无头服装、中背面全身、右头肩肖像）。
- Description: Creates, diagnoses and repairs film assets that must look physically photographed: identity/wardrobe sheets, locations, props, state variants, removing plastic skin. Includes a locked client triptych (2100×1172: headless front wardrobe, full back, head-and-shoulders identity master).
- 用法：“给这个角色做一张客户三联定妆图”；“这张人像太 AI 了，诊断并修复”。
- Usage: “Make the client triptych for this character.” / “This portrait looks AI — diagnose and fix.”

**realm-lock · 真实资产与镜头一致性控制器**

- 简介：写实角色三视图、跨镜一致、非塑料皮肤与材质、反打角度、局部修图。七道不可跳过的闸门，可选 Pillow 做像素变更审计。北极星：保真先于惊艳。
- Description: Photoreal turnarounds, cross-shot consistency, non-plastic skin and materials, reverse angles and local image repair, through seven mandatory gates and optional Pillow pixel-change audits. Fidelity before spectacle.
- 用法：“把这个角色换到反打角度，脸和服装不变”。
- Usage: “Show this character from the reverse angle; keep face and outfit identical.”

**character-clean-extractor · 人物提取与一致性**

- 简介：从参考图中提取指定人物，建立可核查的身份与服装档案，用于三视图、换装、跨图比对与修复脸/手/左右漂移。六种模式：EXTRACT、SHEET、WARDROBE、AUDIT、REPAIR、TRANSFER。MIT 许可。
- Description: Extracts a named character from reference images into an auditable identity and wardrobe profile for turnarounds, outfit transfer, cross-image audits and drift repair. Six modes; MIT licensed.
- 用法：“提取图里穿红外套的人，做身份板”；“AUDIT：这三张为什么不像同一个人”。
- Usage: “Extract the person in the red jacket into an identity sheet.” / “AUDIT: why don't these three look like the same person?”

**packaging-visual-direction · 产品包装视觉方向**

- 简介：为外箱、内包装、小包装与说明书提供以排版、配色、风格为核心的 2–3 条创意方向，含 HEX 色值与面积比例、各面信息层级、版式草图。可从参考图和竞品提取视觉规律。不做印刷刀模。
- Description: Gives 2–3 distinct visual directions for outer boxes, inner packs and manuals: layout, color (HEX plus area ratios), type and style, per-face information hierarchy and layout sketches. Learns from references and competitors; not print-ready dielines.
- 用法：上传产品照片和竞品图：“给我的茶叶礼盒做三个包装方向”。
- Usage: Upload product and competitor photos: “Three packaging directions for my tea gift box.”

**printforge-3d-printing · 图片到 3D 打印**

- 简介：把图片或参考变成可打印候选：单图做 2.5D 多色浮雕 STL/3MF，已有模型做尺寸归一、水平切分、定位销与安全审查。不臆造看不到的背面。
- Description: Turns images into printable candidates: 2.5D multicolor relief STL/3MF from a single image; scale normalization, horizontal split, pegs and safety audit for existing meshes. Never invents unseen backsides.
- 用法：`python -m printforge relief logo.png out/`；`prepare model.glb out --height 120`。
- Usage: `python -m printforge relief logo.png out/` or `prepare model.glb out --height 120`.

**cat-punch-meme · 猫拳表情包**

- 简介：把“猫拳揍他”之类一句话变成缩略图也能一眼看懂的猫拳表情包生图提示词，可配字、选风格与强度。注意：ZIP 名“穿越平行世界爱因斯坦罗森桥系统”与内容不符，建议改名；SKILL.md 缺少标准 frontmatter。
- Description: Turns a one-liner like “cat-punch him” into a thumbnail-readable cat-punch meme/sticker prompt, with caption, style and intensity. Note: the ZIP name doesn't match the content, and the SKILL.md lacks standard frontmatter.
- 用法：“这只橘猫一拳把老板打飞，做成微信表情包，配字：少废话”。
- Usage: “This orange cat punches the boss into orbit — WeChat sticker, caption: ‘Cut the talk.’”

## D. 文字写作 · Writing

**natural-writer · 自然写作助手**

- 简介：中文写作七步法：问清读者与目的、定中心句、选角度与结构、写初稿，再从内容、传播、语言三方面自查；可只拟标题开头或只去 AI 腔。MIT 许可。
- Description: A seven-step Chinese writing flow: clarify reader and goal, set the core sentence, choose angle and structure, draft, then self-check content, reach and language. Can do headlines/openings only or de-AI only. MIT licensed.
- 用法：“写一篇公众号文章，讲小店主怎么用 AI”；“只去掉这篇的 AI 腔，内容不加”。
- Usage: “A WeChat article on how small shop owners can use AI.” / “Remove the AI tone only; add nothing.”

**magic-style-dna v2.0 · 魔法文风写作 DNA**

- 简介：离线作者文风迁移：跨篇分析作者可观察的表达选择，在新主题下保留辨识度。含“传播逆向实验室”复盘上期真实数据，生成可检验的下期方案；支持版本回退与盲测。
- Description: Offline author-style transfer that learns observable writing choices across several pieces and keeps them on new topics. A “reverse-propagation lab” reviews last issue's real metrics to plan a testable next issue; supports rollback and blind tests.
- 用法：粘贴你的 3–5 篇旧文：“学我的文风，写一篇关于……的新文”；“这是上期数据，复盘并规划下期”。
- Usage: Paste 3–5 of your pieces: “Learn my style and write a new one about …” / “Here are last issue's numbers — review and plan the next.”

**public-writing-starter v2.0 · 从选题到成稿**

- 简介：短内容写作（X/微博、小红书、公众号/知乎短文）。A 选题 → B 观点与事实 → C 结构与写作 → D 修改与平台适配，按请求只走需要的一步。
- Description: Short-form writing for X/Weibo, Xiaohongshu and short WeChat/Zhihu pieces: A topic → B claim and facts → C structure and draft → D revise and adapt, running only the step you ask for.
- 用法：“我不知道写什么，帮我选题”；“把这篇转成小红书笔记”。
- Usage: “Help me pick a topic.” / “Turn this into a Xiaohongshu note.”

**纸火·自由写作实验桌 v3.0 · Paper-Fire writing desk (8 sub-skills)**

- 简介：8 个小而精的单点写作工具，各自独立触发。 Eight small single-purpose writing tools, each triggered on its own.

| 子技能 Sub-skill | 做什么 | What it does | 一句话用法 / Say |
| --- | --- | --- | --- |
| first-spark 一句开篇 | 模糊想法直接成完整文章 | Vague idea → full draft | “就这一句，写成文章” |
| format-shift 换个舞台 | 文章/长帖/口播互转 | Convert article ↔ thread ↔ voiceover | “转成 60 秒口播” |
| front-door 第一眼试镜 | 两套标题+开头并推荐一个 | Two title+opening options, one recommended | “给我两个标题开头” |
| opposing-chair 反方入座 | 最强反例磨利观点 | Strongest objection, then a firmer claim | “让反方来挑战” |
| precision-lamp 事实照灯 | 找事实跳跃与过度表述 | Flags factual leaps and overclaims | “发布前核一下事实” |
| raw-to-scene 现场感增强 | 抽象话落进动作与细节 | Abstract lines → concrete scenes | “这段太空，写具体” |
| read-aloud 口耳试读 | 改顺语感与歧义 | Fixes rhythm and ambiguity when read aloud | “念起来别扭，改顺” |
| rhythm-room 文字减重 | 删赘词与机械排比 | Cuts padding and mechanical parallelism | “压到 800 字” |

## E. 思考、Agent 工程与工具 · Thinking, agent engineering & utilities

**bedrock-agora v2.0 · 原点议事引擎**

- 简介：第一性原理决策与 Skill 创作工作台。DECIDE 做复杂决策（事实与假设分离、替代方案、证伪实验）；FORGE 创建或升级任意领域 Skill；BRIDGE 先决定要解决什么，再封装成 Skill。
- Description: First-principles decisions and skill authoring. DECIDE for hard calls (facts vs. assumptions, alternatives, falsifiable tests); FORGE to build or upgrade a skill in any domain; BRIDGE to decide the problem first, then package it as a skill.
- 用法：“DECIDE：我该先做微短剧工具还是角色资产工具”；“FORGE：把我的审稿流程做成 Skill”。
- Usage: “DECIDE: build the micro-drama tool or the asset tool first?” / “FORGE my review process into a skill.”

**faultline-wargame · 断层攻防室**

- 简介：对已有计划、路线或论证做最大强度的压力测试。STRIKE 找最致命的承重假设；WAR-GAME 推演对手反应；REPAIR 最小修复；GATE 给出 GO/PILOT/REVISE/STOP 判决。
- Description: Maximum-strength stress tests of existing plans and arguments. STRIKE finds the load-bearing assumption most likely to break; WAR-GAME simulates competitor moves; REPAIR proposes minimal fixes; GATE returns GO/PILOT/REVISE/STOP.
- 用法：“STRIKE 这份商业计划，只给我最致命的一个漏洞”。
- Usage: “STRIKE this business plan — just the single most fatal flaw.”

**idea-prism · 轻量思想迁用**

- 简介：从指定的长对话中提炼可追溯的“思想卡”，区分用户确认与助手建议，并在新业务讨论中检验适用边界。只做判断，不做方案。
- Description: Distills a long conversation into a traceable “idea card” that separates what you confirmed from what the assistant suggested, then tests where those ideas apply in a new discussion. Judgments only, no plans.
- 用法：粘贴聊天记录：“提炼这段聊天”；然后“把思想卡迁用到我的包装生意上”。
- Usage: Paste a chat: “Distill this.” Then “Apply the card to my packaging business.”

**vibe-coding-intent-compiler · 意图编译器**

- 简介：把口语化、反复变化的软件需求编译成执行合同：区分“只讨论”与“开做”，保住不变量，把“高级一点”变成可测验收标准，防止越改越偏。
- Description: Compiles colloquial, shifting software requests into an execution contract: separates “just discuss” from “build it”, preserves invariants across revisions, and turns vague taste into testable acceptance criteria.
- 用法：“先设计，别动代码”；“只改登录页按钮，其他别动”。
- Usage: “Design first, don't touch code.” / “Change only the login button; leave everything else.”

**sharp-dialogue-protocol · 高信噪比对话协议**

- 简介：防止长对话漂移与空话的对话协议，带任务分级（简单任务直接放行、复杂工程强制澄清）与 checkpoint 断点续传。内容偏抽象，可移植性一般。
- Description: A protocol against drift and filler in long sessions, with task triage (simple asks pass through, complex engineering gets challenged) and checkpoint save/resume. Fairly abstract; limited portability.
- 用法：“读取 checkpoint，断点继续”。
- Usage: “Load the checkpoint and resume.”

**agent-instruction-optimizer v2.0 · 指令优化器**

- 简介：优化 system prompt、AGENTS.md、Skill 与 Agent 提示词。每段按 KEEP/COMPRESS/ROUTE/CLARIFY/REMOVE 处理，追求“单位指令的任务完成率”而非单纯精简；附目录扫描与断链检查脚本。
- Description: Optimizes system prompts, AGENTS.md, skills and agent prompts, tagging each block KEEP/COMPRESS/ROUTE/CLARIFY/REMOVE to raise task completion per instruction, not mere brevity. Includes a scan and broken-link checker.
- 用法：“审计并重写这个 SKILL.md，保留所有安全约束”。
- Usage: “Audit and rewrite this SKILL.md; keep every safety constraint.”

**skill-sentinel · Skill 安全哨兵**

- 简介：离线只读审计 Skill 的 SKILL.md、脚本、Hooks、依赖与 ZIP，查提示注入、密钥泄露、远程代码执行、数据外传与供应链风险；可做 SHA256 变更复检。绝不运行被审代码。
- Description: Offline, read-only audit of skills (SKILL.md, scripts, hooks, dependencies, ZIPs) for prompt injection, leaked secrets, remote code execution, exfiltration and supply-chain risk, with SHA256 re-checks. Never runs the audited code.
- 用法：“安装前审计这个文件夹里所有 ZIP”——建议对朋友给你的技能先跑一遍。
- Usage: “Audit every ZIP in this folder before I install them” — worth running on the skills friends gave you.

**library-steward · 知识库管家**

- 简介：接入并管理本地知识库/素材库：摸底、全文检索（SQLite FTS5，中文可搜）、按行号页码定位、入库、来源登记、快照与回滚。仅依赖 Python 标准库。
- Description: Connects and manages a local knowledge or asset library: survey, full-text search (SQLite FTS5, Chinese-ready), line/page location, ingest, source registry, snapshots and rollback. Python standard library only.
- 用法：“接入我的风格库 D:/style-lib”；“哪一页讲过过肩镜头？”
- Usage: “Connect my style library at D:/style-lib.” / “Which page covers over-the-shoulder shots?”

**infinite-canvas-function-architect · 无限画布功能架构师**

- 简介：把杂乱产品需求转成可编辑的无限画布：先建立规范图模型（目标、模块、功能、流程、依赖、风险、缺口），再渲染成单文件 HTML 或 React Flow。MIT 许可。
- Description: Turns messy product notes into an editable infinite canvas: builds a canonical graph (goals, modules, features, flows, dependencies, risks, gaps) first, then renders single-file HTML or React Flow. MIT licensed.
- 用法：“把这些功能点做成无限画布，标出依赖和缺口”——很适合你规划产品时用。
- Usage: “Map these features on an infinite canvas with dependencies and gaps” — handy for planning your products.

**codex-clean · Agent 缓存清理**

- 简介：只清理 Codex、Claude Code、Pi 等编码 Agent 自己产生的可重建缓存与日志，对日志库做 VACUUM 与 WAL 截断。默认只读扫描、逐项确认，不碰会话、配置和项目。
- Description: Cleans only regenerable caches and logs created by coding agents (Codex, Claude Code, Pi), with SQLite VACUUM and WAL truncation. Read-only scan by default, per-item confirmation; never touches sessions, config or projects.
- 用法：“Codex 占空间太大，帮我清理”；或 `--target all --json` 先预览。
- Usage: “Codex is eating my disk — clean it”, or preview with `--target all --json`.

**download-anything · 万物下载（第三方）**

- 简介：用 yt-dlp、aria2、gallery-dl、spotdl 等工具查找并下载视频、电子书、论文、软件、字体等，含中文网盘搜索与搜索技巧。作者 keystone。部分用法涉及版权风险。
- Description: Finds and downloads video, ebooks, papers, software, fonts and more with yt-dlp, aria2, gallery-dl and spotdl, including Chinese cloud-drive search. By “keystone”. Parts of it invite copyright risk.
- 用法：“下载这个链接的视频”；“找免费可商用的字体”。只用于你有权下载的内容。
- Usage: “Download the video at this link.” / “Find free commercial-use fonts.” Use only for content you have rights to.

## 非技能材料 · Non-skill materials

这 9 个文件没有 SKILL.md，不能作为技能安装，故不参与排名。建议移到单独文件夹（如 `materials/`），并处理标注的风险。 These 9 files have no SKILL.md, so they aren't installable skills and aren't ranked. Move them to a separate folder and handle the flagged risks.

| 文件 File | 是什么 | What it is | 建议 Action |
| --- | --- | --- | --- |
| `AI-Learning-12-Weeks-v1(1).zip` | 12 周 AI 学习课程，每周 8–10 小时 | 12-week personal AI course | 保留为学习资料 Keep as study material |
| `Survival_Cast_AssetKit_v1.zip` | 大逃杀电影 18 人角色资产包：Schema、提示词生成器 | 18-character cast kit for a battle-royale film | 项目产物；其 Schema 可纳入资产产品 Project output; its schema can seed the asset product |
| `awesome-opus-5.5-video-main(4).zip` | 第三方整理的 962 个 Opus 5.5 视频案例清单 | Third-party list of 962 Opus 5.5 video cases | 参考材料，不宜重新发布 Reference only; don't republish |
| `lordaeron-lastwatch-v1.0(3).zip` | 《魔兽争霸 III》同人塔防小游戏（单个 HTML） | Warcraft III fan tower-defense game | 涉暴雪 IP，不可商用 Blizzard IP; never commercial |
| `skill-control-center-v1.0.0(1)(1).zip` | Tauri 桌面应用的界面覆盖补丁（技能控制中心） | UI overlay patch for a Tauri skill-manager app | 需配合其源码仓库；可作产品四的前端 Needs its source repo; candidate front end for Product 4 |
| `映衡｜导演的创作与判断协作协议.md` | 给影视导演用的 AI 协作系统提示词 | System prompt for a director's AI collaborator | 可转成 Skill（用 bedrock-agora FORGE） Could become a skill via FORGE |
| `AI影视创作知识库_搭建方案_v4(2).md` | 本地 AI 影视知识库的施工方案 | Build plan for a local film knowledge base | 与 library-steward 合并实施 Implement together with library-steward |
| `韩剧双Skill独立审查报告-2026-10-20(2).md` | 两个韩剧技能的审查报告（规则 8.5/10，量产就绪 6.3/10） | Audit report on the two K-drama skills | 移入对应技能的 docs/ Move into those skills' docs |
| `Son-of-Seagal.pdf` | Matt R. Allen 的英文电影剧本（2016 稿） | Matt R. Allen's 2016 screenplay draft | **他人版权作品，按你的要求保留** Someone else's copyrighted script; kept at your request |
