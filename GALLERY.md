# 山河入版

- 185 张原创 AI 套色木刻风格画作：01–20 想象山河；21–40 中国名胜；41–60 旅游城市；61–80 山河里的生活；81–100 节日与民俗；101–120 海外风光；121–125 日本庭院与鸟居；126–130 海浪与潮汐；131–185 十一城五景。
- 生成器：内置 image_gen；用户附件仅作风格参考。原图 incoming/；全部准确提示词 prompts.json。第100张源文件名 festival-100.png，保证模板的文件排序中置于末尾；ZIP内仍为100.png。
- 用户偏好：木刻刀痕、套色、纸张肌理；颜色多样变化；城市批次避免前批景点重复；允许 subagent 并行。
- 页面保持 build-gallery 模板，editorial 暖白主题、grid。山野/江湖/海岸/田园/中国名胜/旅游城市/山河里的生活/节日与民俗/海外风光/日本庭院与鸟居/海浪与潮汐十一类，另增上海、苏州、成都、京都、首尔、大阪、马德里、塞维利亚、巴塞罗那、里斯本、格拉纳达城市分类，每城5张。下载和分享开启、统计关闭。
- 预览：http://127.0.0.1:4327；正式地址：https://shanhe-gallery.xiaosang.cc/；源码：https://github.com/holynova/shanhe-gallery。
- 2026-10-05 新增：生活组20幅，清晨/途中/暮色/夜里各5幅；节日组20幅，涵盖春节、元宵、清明、端午、七夕、中秋、重阳、腊八、小年、冬至、泼水节、火把节、藏历新年等节庆场景。
- 前60张原图SHA256及图片说明逐项保持原样。100张原图哈希全部唯一，新图逐图或总览目视检查通过。
- 验证：模板一致性通过；类型检查0错误/警告；7项测试通过；最终ingest/validate/build成功；100张、1500个响应式文件、261669813 bytes输出；原始PNG不进入dist。
- 浏览器：两个新增分类各20张缩略图全部解码；全部加载100张；灯箱蒸年糕→贴春联，反向环回藏历新年；Esc关闭；下载HTTP200；390px无横向溢出；无控制台错误。
- outputs/中5份原图ZIP各20张。新增两份已完整解压校验。life-overview.jpg、festivals-overview.jpg为新增总览，festivals-desktop-preview.png、festivals-mobile-preview.png为网页截图。

后续修改同一站点。编辑content/后npm run build；已有派生图片复用缓存。

## 海外风光批次

- 20幅已完成并目视检查；原有100幅原图哈希与图片说明保持原样。内置image_gen提示词已追加至prompts.json，资料见overseas-selection.md。
- 模板一致性通过；ingest/validate/build通过：120张，新增生成20张、缓存复用100张，1800个响应式文件，312249193 bytes输出。
- 浏览器：海外20张全部解码；灯箱马特洪峰→劳特布龙嫩、反向环回米尔福德；Esc关闭；下载HTTP200；全部加载120张；390px无溢出；控制台无错误。
- 海外风光-20张原图.zip含20张，完整校验通过。overseas-overview.jpg为总览，overseas-desktop-preview.png和overseas-mobile-preview.png为展示截图。

## 日本庭院与海洋补充批次

- 新增10张：枯山水、池泉回游、秋枫茶庭、海上鸟居、林间参道；浪峰、礁岸潮涌、透光浅湾、风暴之后、月下潮汐。日本画面为虚构风格场景，不标注真实寺院或神社。
- 内置image_gen独立生成，逐图/总览目视通过。原有120张的原图SHA256及图片说明保持原样，130原图哈希全唯一；提示词完整追加。
- 模板一致性通过；ingest/validate/build通过：130张，新增生成10、复用120，1950个响应式文件，339268954 bytes输出；原始PNG不进入dist。
- 浏览器：两个新分类各5张全部解码；全部加载130；灯箱浪峰→礁岸潮涌、反向环回月下潮汐；Esc关闭，下载200；390px无横向溢出；无控制台错误。
- 日本庭院与海洋-10张原图.zip包含10 PNG，完整解压检查通过；supplement-overview.jpg为总览；supplement-desktop-preview.png、supplement-mobile-preview.png为网页截图。

## 十一城五景批次

- 新增55张，11城各5张；严格使用3个subagent同时生成，交付20+20+15。内置image_gen逐幅生成；180编辑去除铭文，完整生成和编辑提示词保存在prompts.json。
- 原有130张原图SHA256及图片说明逐项保持原样；185原图哈希全唯一。每张1122×1402，每城总览已目视检查；城市选题与官方轻量参考见cityset-selection.md。
- 模板一致性通过，类型检查0错误/警告，7项测试通过；ingest/validate/build成功：185张、新增生成55张、复用130张，2775个响应式文件，490570128 bytes输出；原始PNG不进入dist。
- 浏览器逐城验证11类各5张全部解码；全部加载185张。灯箱豫园→武康大楼、反向环回朱家角；Esc关闭并归还焦点；下载HTTP200；390px无横向溢出；控制台0错误/警告。
- 十一城-55张原图.zip及11份城市原图ZIP各5张，均完整校验通过。cityset-overview.jpg为55张总览；cityset-desktop-preview.png、cityset-mobile-preview.png为网页截图。当前本地预览已刷新185张并展示上海分类。

## 首次正式发布

目标 https://shanhe-gallery.xiaosang.cc/；GitHub holynova/shanhe-gallery，main 分支。本次发布技能要求 footer 增加 GitHub 链接与构建注入版本，为模板外观约束的具体授权例外，不修改网格和导航布局。保留明确 analytics.enabled=false 配置。账户100个Custom Domain已满，采用同一正式子域名的代理DNS与精确Worker Route，不移除其他项目。

2026-10-06 发布完成：v0.1.1，main 运行源码提交0a42c38。项目 Worker shanhe-gallery，版本25d0fca9-553d-486e-a0c9-384dfb780615；正式域名HTTPS200，185张、公网11城市各5张、灯箱/下载/390px布局通过，控制台0错误。18项JS/CSS/图片/favicon公网哈希与构建一致。二维码实际解码通过。
作品集 master 提交073d7f4，xiaosang-portfolio版本e8c08f55-d6aa-4489-8bb8-0e6019dd57d5；线上完整JSON与master一致，截图哈希相同，卡片点击打开正式画廊。Profile main 提交ee13366，公开页面已显示新行及正确Repo/Demo链接。统计沿用关闭设置；未开启Pages或自动发布。
