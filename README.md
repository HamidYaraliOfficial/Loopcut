<p align="center">
  <a href="https://github.com/HamidYaraliOfficial/Loopcut">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset=".github/readme/lockup-dark.png">
      <img alt="Loopcut" src=".github/readme/lockup-light.png" width="340">
    </picture>
  </a>
</p>

<h3 align="center">You're the artist. Loopcut's the technician.</h3>

<p align="center">
  An open-source AI agent inside Blender. Describe the technical work in a sentence; Loopcut writes and runs the Python, shows you every step, checks the viewport, and leaves the creative decisions to you.
</p>

<p align="center">
  **فارسی:** شما هنرمند هستید؛ Loopcut کارهای فنی را انجام می‌دهد. Loopcut یک عامل هوش مصنوعی متن‌باز درون Blender است. کار فنی موردنظر را در یک جمله توضیح دهید؛ Loopcut کد Python را می‌نویسد و اجرا می‌کند، مراحل را نمایش می‌دهد، نتیجه را در نمای سه‌بعدی بررسی می‌کند و تصمیم‌های خلاقانه را به شما واگذار می‌کند.
  <br>
  **中文：** 您负责创作，Loopcut 负责技术工作。Loopcut 是集成在 Blender 中的开源 AI 智能代理。您只需用一句话描述技术任务，Loopcut 就会编写并运行 Python 代码、展示每一步操作、检查 3D 视口，并将创意决策留给您。
</p>

<p align="center">
  **فارسی:** توسعه‌دهنده و نگه‌دارنده: حمید یارعلی · <a href="https://github.com/HamidYaraliOfficial/Loopcut">مخزن گیت‌هاب Loopcut</a>
  <br>
  **English:** Developer and maintainer: Hamid Yarali · <a href="https://github.com/HamidYaraliOfficial/Loopcut">Loopcut GitHub repository</a>
  <br>
  **中文：** 开发者与维护者：Hamid Yarali（حمید یارعلی）· <a href="https://github.com/HamidYaraliOfficial/Loopcut">Loopcut GitHub 仓库</a>
</p>

<p align="center">
  <a href="https://github.com/HamidYaraliOfficial/Loopcut">GitHub / English</a> ·
  <a href="https://github.com/HamidYaraliOfficial/Loopcut">گیت‌هاب / فارسی</a> ·
  <a href="https://github.com/HamidYaraliOfficial/Loopcut">GitHub / 中文</a> ·
  <a href="#install">Install / نصب / 安装</a> ·
  <a href="#your-model-or-ours">Models / مدل‌ها / 模型</a> ·
  <a href="loopcut/DEVELOPING.md">Developer guide / راهنمای توسعه / 开发指南</a>
</p>

<p align="center">
  <a href="https://github.com/HamidYaraliOfficial/Loopcut/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/HamidYaraliOfficial/Loopcut?style=flat-square&color=4a95a3&label=release"></a>
  <a href="https://github.com/HamidYaraliOfficial/Loopcut/actions/workflows/tests.yml"><img alt="Tests" src="https://img.shields.io/github/actions/workflow/status/HamidYaraliOfficial/Loopcut/tests.yml?branch=main&style=flat-square&label=tests"></a>
  <a href="https://github.com/HamidYaraliOfficial/Loopcut/releases"><img alt="Downloads" src="https://img.shields.io/github/downloads/HamidYaraliOfficial/Loopcut/total?style=flat-square&color=df8b37"></a>
  <img alt="Blender 5.2" src="https://img.shields.io/badge/Blender-5.2-4a95a3?style=flat-square">
  <img alt="macOS and Windows" src="https://img.shields.io/badge/platforms-macOS%20%7C%20Windows-2a2a2e?style=flat-square">
  <a href="LICENSE"><img alt="License: GPL-3.0-or-later" src="https://img.shields.io/badge/license-GPL--3.0--or--later-2a2a2e?style=flat-square"></a>
</p>

<p align="center">
  <a href="https://github.com/HamidYaraliOfficial/Loopcut"><img alt="Loopcut inside Blender: a three-point light rig set up from one message, with the scene changes listed and one click to undo them" src=".github/readme/hero.webp" width="960"></a>
</p>

---

## Table of contents / فهرست مطالب / 目录

- [What it does / قابلیت‌ها / 功能介绍](#what-it-does)
- [Installation / نصب / 安装](#install)
- [Choose an AI model / انتخاب مدل هوش مصنوعی / 选择 AI 模型](#your-model-or-ours)
- [Example prompts / نمونه درخواست‌ها / 示例指令](#what-to-ask-it)
- [How a turn works / روند اجرای درخواست / 单次任务的工作流程](#how-a-turn-works)
- [Privacy and conversation history / حریم خصوصی و تاریخچه / 隐私与对话历史](#privacy-and-conversation-history)
- [Build from source / ساخت از سورس / 从源代码构建](#building-from-source)
- [Contributing / مشارکت / 参与贡献](#contributing)
- [Bundled add-ons / افزونه‌های همراه / 内置扩展](#bundled-add-ons)
- [License and product name / مجوز و نام محصول / 许可证与产品名称](#license-and-name)

---

## What it does

### English
Loopcut is an AI-assisted technical workflow for Blender. Instead of manually repeating routine scene-management and setup operations, describe the desired result in natural language. Loopcut can prepare Python code for the task, show you the proposed steps, execute them after approval, and report the changes measured from the actual scene.

- **Describe technical work in a sentence.** Rename objects according to their materials, organize objects into collections, correct normals, reorder modifiers, connect constraints and drivers, unwrap and pack UVs, create lighting rigs, configure render presets, or batch-export assets.
- **Review each step before it runs.** The generated code waits for approval before execution, unless you choose to stop being asked during the current conversation. The goal is to make the proposed operation visible rather than silently changing the scene.
- **Inspect actual scene changes.** The “Scene changes” summary is based on the scene after execution and identifies what was added, removed, or changed. It is not simply a restatement of the model's response.
- **Let the agent inspect its work.** Loopcut can capture the Blender viewport and use that view to check the result. You can also attach a reference image and compare it with a viewport capture to guide adjustments.
- **Undo a task as a checkpoint.** Each turn that changes the scene creates a checkpoint. **Undo all** restores the scene and conversation to their state before that turn. The project description states that your `.blend` file is not written to as part of this restore process.
- **Give context about the current scene.** The active file, mode, selection, and objects are passed with each message. Use `@Name` to refer to a particular object, material, or collection. Installed add-ons can be visible to the agent and may be used where applicable.
- **Choose how the model runs.** Use a provider API key, connect a model running on your own machine, or sign in to use hosted models, depending on your preferred setup.
- **Stay in a Blender-based workflow.** Loopcut is based on Blender 5.2 and adds a dedicated panel and project-specific changes. On first launch, you can import settings, add-ons, keymap, themes, and startup-file preferences from an existing Blender setup, or start fresh. The application includes an update flow.

### فارسی
Loopcut یک گردش‌کار فنی مبتنی بر هوش مصنوعی برای Blender است. به‌جای تکرار دستی عملیات روزمره مدیریت صحنه و آماده‌سازی پروژه، نتیجه موردنظر خود را با زبان طبیعی توضیح دهید. Loopcut می‌تواند کد Python لازم را آماده کند، مراحل پیشنهادی را نشان دهد، پس از تأیید شما آن‌ها را اجرا کند و تغییرات را بر اساس وضعیت واقعی صحنه گزارش دهد.

- **شرح کار فنی در یک جمله:** نام‌گذاری مجدد اشیا بر اساس جنس متریال، دسته‌بندی اشیا در Collectionها، اصلاح نرمال‌ها، مرتب‌سازی Modifierها، تنظیم Constraintها و Driverها، بازکردن و بسته‌بندی UVها، ساخت چیدمان نور، تنظیم پیش‌فرض‌های رندر و خروجی‌گرفتن گروهی از دارایی‌ها.
- **بررسی مراحل پیش از اجرا:** کد تولیدشده پیش از اجرا منتظر تأیید شما می‌ماند؛ مگر اینکه در همان گفت‌وگو انتخاب کنید که دیگر برای هر مرحله تأیید درخواست نشود. هدف این است که عملیات پیشنهادی قابل مشاهده باشد و صحنه بدون اطلاع شما تغییر نکند.
- **مشاهده تغییرات واقعی صحنه:** خلاصه «Scene changes» پس از اجرا از وضعیت خود صحنه تهیه می‌شود و موارد اضافه‌شده، حذف‌شده یا تغییرکرده را مشخص می‌کند؛ این خلاصه صرفاً تکرار پاسخ متنی مدل نیست.
- **بررسی نتیجه توسط عامل هوش مصنوعی:** Loopcut می‌تواند از نمای Blender تصویر بگیرد و نتیجه را بررسی کند. همچنین می‌توانید تصویر مرجع را ضمیمه کنید و آن را کنار تصویر نمای سه‌بعدی قرار دهید تا اصلاحات دقیق‌تری انجام شود.
- **بازگشت به نقطه بازیابی:** هر نوبتی که صحنه را تغییر دهد، یک نقطه بازیابی ایجاد می‌کند. گزینه **Undo all** صحنه و گفت‌وگو را به وضعیت پیش از آن نوبت بازمی‌گرداند. طبق توضیحات پروژه، این فرایند فایل `.blend` شما را بازنویسی نمی‌کند.
- **استفاده از اطلاعات صحنه جاری:** فایل فعال، حالت کاری، انتخاب فعلی و اشیا همراه هر پیام در اختیار عامل قرار می‌گیرند. با نوشتن `@Name` می‌توانید به یک شیء، متریال یا Collection مشخص اشاره کنید. افزونه‌های نصب‌شده نیز ممکن است در دسترس عامل باشند و در صورت نیاز استفاده شوند.
- **انتخاب روش اجرای مدل:** بسته به تنظیمات دلخواه، می‌توانید کلید API ارائه‌دهنده را وارد کنید، به مدل محلی روی رایانه خود متصل شوید یا از مدل‌های میزبانی‌شده استفاده کنید.
- **حفظ گردش‌کار در Blender:** Loopcut بر پایه Blender 5.2 ساخته شده و یک پنل اختصاصی و تغییرات مرتبط با پروژه به آن اضافه می‌کند. در اولین اجرا می‌توانید تنظیمات، افزونه‌ها، میان‌برها، پوسته‌ها و فایل آغازین Blender قبلی را وارد کنید یا از تنظیمات تازه شروع کنید. برنامه همچنین فرایند به‌روزرسانی داخلی دارد.

### 中文
Loopcut 是面向 Blender 的 AI 辅助技术工作流。无需反复手动执行常见的场景管理和准备操作，只需用自然语言描述目标。Loopcut 可以生成完成任务所需的 Python 代码、展示拟执行步骤、在获得批准后运行，并根据实际场景状态汇报变更。

- **用一句话描述技术任务：** 按材质重命名对象、将对象整理到集合中、修正法线、调整修改器顺序、配置约束和驱动器、展开并打包 UV、创建灯光布置、设置渲染预设，或批量导出资源。
- **执行前检查每一步：** 生成的代码会在运行前等待您批准；除非您选择在当前对话中不再逐步询问。设计目标是让操作过程可见，而不是在没有说明的情况下悄悄修改场景。
- **核对真实场景变更：** “Scene changes”摘要根据执行后的场景生成，并列出新增、删除或修改的内容，而不只是复述模型的文字回答。
- **让智能代理检查结果：** Loopcut 可以捕获 Blender 视口画面并据此检查结果。您也可以附加参考图片，将参考图与视口截图进行对比，以指导后续调整。
- **通过检查点撤销任务：** 每次改变场景的交互都会创建一个检查点。**Undo all** 会将场景和对话恢复到该轮操作之前的状态。项目说明指出，这种恢复操作不会写入或覆盖您的 `.blend` 文件。
- **利用当前场景上下文：** 每条消息都会携带当前文件、模式、选择状态和对象信息。输入 `@Name` 可以指向特定对象、材质或集合。智能代理也可以查看已安装的扩展，并在适用时使用它们。
- **选择模型运行方式：** 根据您的配置偏好，可以使用服务提供商的 API 密钥、连接本机运行的模型，或登录使用托管模型。
- **继续使用 Blender 工作流：** Loopcut 基于 Blender 5.2，并增加专用面板和项目相关修改。首次启动时，可以从现有 Blender 安装导入偏好设置、扩展、快捷键映射、主题和启动文件，也可以选择全新设置。应用程序还提供内置更新流程。

---

## Install

### English
Download the latest available build from the [GitHub Releases page](https://github.com/HamidYaraliOfficial/Loopcut/releases/latest). Choose the package that matches your operating system and processor.

| Platform | File | Installation notes |
|---|---|---|
| macOS (Apple silicon) | `loopcut-<version>-arm64.dmg` | Open the disk image and drag Loopcut to Applications. |
| Windows (64-bit) | `loopcut-<version>-windows64.msi` or `.zip` | Run the installer, or extract the ZIP archive to a location of your choice. |

**First-launch security notices:** The builds are currently described as unsigned, so your operating system may show a security warning on the first launch.

- **macOS:** If macOS says it “could not verify” Loopcut, click **Done**, then open **System Settings → Privacy & Security → Open Anyway** if you trust the build you downloaded. An alternative shown by the project is the Terminal command `xattr -dr com.apple.quarantine /Applications/Loopcut.app`. Check the application path before running the command.
- **Windows:** If SmartScreen appears, verify that you downloaded the intended release. The documented flow is **More info → Run anyway**.

**First-run setup:** Choose **Import Blender 5.2 Settings** to bring over preferences, add-ons, keymap, themes, and the startup file from an existing Blender setup, or choose **Start Fresh**. Connect an AI model to begin. The Loopcut panel docks to the right of the 3D Viewport. The documented shortcut to focus it is `⌘ L` on macOS and `Ctrl Alt L` on Windows.

**Updates:** Later updates can be installed from inside the application using **Restart to update**. The project description says subsequent updates do not trigger the same first-launch warning again.

### فارسی
آخرین نسخه موجود را از صفحه [انتشارهای گیت‌هاب](https://github.com/HamidYaraliOfficial/Loopcut/releases/latest) دریافت کنید. بسته‌ای را انتخاب کنید که با سیستم‌عامل و نوع پردازنده شما سازگار باشد.

| سیستم‌عامل | فایل | توضیحات نصب |
|---|---|---|
| macOS با پردازنده Apple Silicon | `loopcut-<version>-arm64.dmg` | فایل DMG را باز کنید و Loopcut را به پوشه Applications بکشید. |
| ویندوز ۶۴ بیتی | `loopcut-<version>-windows64.msi` یا `.zip` | نصب‌کننده را اجرا کنید یا فایل ZIP را در مسیر دلخواه استخراج کنید. |

**هشدار امنیتی در اولین اجرا:** طبق توضیحات پروژه، نسخه‌های فعلی امضای دیجیتال ندارند؛ بنابراین ممکن است سیستم‌عامل در اولین اجرا هشدار امنیتی نمایش دهد.

- **macOS:** اگر پیام «could not verify» نمایش داده شد، روی **Done** کلیک کنید و در صورت اطمینان از منبع فایل، مسیر **System Settings → Privacy & Security → Open Anyway** را دنبال کنید. روش جایگزین مستندشده در پروژه اجرای دستور `xattr -dr com.apple.quarantine /Applications/Loopcut.app` در Terminal است. پیش از اجرای دستور، مسیر برنامه را بررسی کنید.
- **Windows:** اگر SmartScreen نمایش داده شد، ابتدا مطمئن شوید فایل را از صفحه انتشار موردنظر دریافت کرده‌اید. مسیر مستندشده عبارت است از **More info → Run anyway**.

**تنظیمات اولین اجرا:** برای واردکردن ترجیحات، افزونه‌ها، میان‌برها، پوسته‌ها و فایل آغازین از نصب قبلی Blender، گزینه **Import Blender 5.2 Settings** را انتخاب کنید؛ در غیر این صورت **Start Fresh** را بزنید. سپس یک مدل هوش مصنوعی را متصل کنید. پنل Loopcut در سمت راست نمای سه‌بعدی قرار می‌گیرد. میان‌بر مستندشده برای تمرکز روی پنل در macOS برابر `⌘ L` و در ویندوز `Ctrl Alt L` است.

**به‌روزرسانی:** نسخه‌های بعدی از داخل برنامه و با گزینه **Restart to update** نصب می‌شوند. طبق توضیحات پروژه، پس از به‌روزرسانی اولیه همان هشدار امنیتی نخستین اجرا دوباره نمایش داده نمی‌شود.

### 中文
请从 [GitHub Releases 发布页面](https://github.com/HamidYaraliOfficial/Loopcut/releases/latest) 下载当前可用的最新版本，并选择与操作系统和处理器相匹配的安装包。

| 平台 | 文件 | 安装说明 |
|---|---|---|
| macOS（Apple 芯片） | `loopcut-<version>-arm64.dmg` | 打开 DMG 磁盘映像，并将 Loopcut 拖到 Applications 文件夹。 |
| Windows（64 位） | `loopcut-<version>-windows64.msi` 或 `.zip` | 运行安装程序，或将 ZIP 压缩包解压到所需位置。 |

**首次启动时的安全提示：** 项目说明指出，目前的构建版本尚未签名，因此操作系统可能会在首次启动时显示安全警告。

- **macOS：** 如果系统提示无法验证 Loopcut，请点击 **Done**；确认下载文件可信后，进入 **System Settings → Privacy & Security → Open Anyway**。项目还提供了 Terminal 命令 `xattr -dr com.apple.quarantine /Applications/Loopcut.app` 作为替代方法。执行命令前请核对应用程序路径。
- **Windows：** 如果出现 SmartScreen，请先确认下载的是目标版本。文档所述操作路径为 **More info → Run anyway**。

**首次运行设置：** 选择 **Import Blender 5.2 Settings**，可导入现有 Blender 配置中的偏好设置、扩展、快捷键映射、主题和启动文件；也可以选择 **Start Fresh** 从头开始。随后连接 AI 模型即可使用。Loopcut 面板停靠在 3D 视口右侧。文档给出的面板聚焦快捷键为 macOS 上的 `⌘ L`，以及 Windows 上的 `Ctrl Alt L`。

**更新：** 后续版本可以在应用内部通过 **Restart to update** 安装。项目说明称，完成首次启动后，后续更新不会再次触发相同的首次启动警告。

---

## Your model or ours

### English
Loopcut offers several ways to connect an AI model. Choose the approach that fits your provider access, privacy requirements, and available hardware.

| Option | How it works | Important details |
|---|---|---|
| **Bring your own key** | Enter an API key from Anthropic (Claude, including prompt caching) or another OpenAI-compatible provider. | The key is stored locally in a user-only file, and requests are sent directly to the selected provider. The project says no Loopcut account is required for this option. |
| **Run a model locally** | Connect Loopcut to a model running on your own computer or GPU, for example through Ollama, LM Studio, llama.cpp, or vLLM. | This option is intended to work offline; model requests do not need to leave your local environment. Availability and performance depend on your model and hardware setup. |
| **Hosted by Loopcut** | Sign in through the app and use the hosted model options. | The project describes **Fast** and **Pro** modes using models selected for Blender work, with a free tier included. Check the repository for current details and availability. |

With your own provider key or a local model, the project states that prompts and scenes do not pass through Loopcut's servers. With hosted models, a gateway relays requests and retains token counts for billing, rather than prompts or scene data, according to the project description.

### فارسی
Loopcut چند روش برای اتصال به مدل هوش مصنوعی ارائه می‌دهد. روشی را انتخاب کنید که با دسترسی شما به ارائه‌دهندگان مدل، نیازهای حریم خصوصی و سخت‌افزار موجود سازگار باشد.

| گزینه | روش کار | نکات مهم |
|---|---|---|
| **استفاده از کلید شخصی** | کلید API مربوط به Anthropic (از جمله Claude با پشتیبانی از prompt caching) یا یک ارائه‌دهنده سازگار با OpenAI را وارد کنید. | کلید در یک فایل محلی با دسترسی محدود به کاربر ذخیره می‌شود و درخواست‌ها مستقیماً به ارائه‌دهنده انتخاب‌شده ارسال می‌شوند. طبق توضیحات پروژه، برای این روش به حساب Loopcut نیاز ندارید. |
| **اجرای مدل به‌صورت محلی** | Loopcut را به مدلی متصل کنید که روی رایانه یا GPU خودتان اجرا می‌شود؛ برای نمونه از طریق Ollama، LM Studio، llama.cpp یا vLLM. | این روش برای کار آفلاین طراحی شده است و درخواست‌های مدل لازم نیست از محیط محلی شما خارج شوند. امکان اجرا و سرعت به مدل و سخت‌افزار شما بستگی دارد. |
| **استفاده از مدل‌های میزبانی‌شده Loopcut** | از داخل برنامه وارد شوید و گزینه‌های میزبانی‌شده را استفاده کنید. | طبق توضیحات پروژه، حالت‌های **Fast** و **Pro** با مدل‌های انتخاب‌شده برای کارهای Blender ارائه می‌شوند و سطح رایگان نیز وجود دارد. برای اطلاعات و دسترسی فعلی، مخزن را بررسی کنید. |

طبق توضیحات پروژه، هنگام استفاده از کلید ارائه‌دهنده شخصی یا مدل محلی، پیام‌ها و صحنه‌ها از سرورهای Loopcut عبور نمی‌کنند. در روش مدل میزبانی‌شده، یک درگاه درخواست‌ها را منتقل می‌کند و برای محاسبه هزینه، تعداد توکن‌ها را نگه می‌دارد؛ نه متن درخواست‌ها یا اطلاعات صحنه.

### 中文
Loopcut 支持多种 AI 模型连接方式。请根据您拥有的模型服务权限、隐私要求和硬件条件选择合适的方案。

| 方案 | 工作方式 | 重要说明 |
|---|---|---|
| **使用自己的 API 密钥** | 输入 Anthropic（包括支持提示缓存的 Claude）或其他 OpenAI 兼容服务商的 API 密钥。 | 密钥保存在本地、仅当前用户可访问的文件中，请求会直接发送给所选服务商。项目说明称，此方式不需要 Loopcut 账户。 |
| **本地运行模型** | 将 Loopcut 连接到在自己的电脑或 GPU 上运行的模型，例如通过 Ollama、LM Studio、llama.cpp 或 vLLM。 | 此方案旨在支持离线使用；模型请求无需离开本地环境。实际可用性和性能取决于模型及硬件配置。 |
| **使用 Loopcut 托管模型** | 在应用中登录并使用托管模型选项。 | 项目说明提供面向 Blender 工作的 **Fast** 和 **Pro** 模式，并包含免费层级。当前功能和可用性请以仓库中的最新说明为准。 |

根据项目描述，使用自己的服务商密钥或本地模型时，提示内容和场景数据不会经过 Loopcut 服务器。使用托管模型时，网关会转发请求，并为计费保留 token 数量，而不是保存提示内容或场景数据。

---

## What to ask it

### English
You can describe the intended change in everyday language. The following examples illustrate the kinds of technical tasks documented for Loopcut; adapt names and details to your own scene.

**Organize a scene and build lighting**
```text
Rename everything after what it is, put the lights in their own collection, and set up a three-point rig around the bottle.
```

**Apply transforms and clean geometry data**
```text
Apply scale on everything, fix the flipped normals, and purge orphan data.
```

**Set up character rigging**
```text
Add an IK chain to the legs with pole targets, and mirror the naming to .L/.R.
```

**Match a reference and prepare a render**
```text
Match the framing of the reference photo I attached and set up a product-shot render preset at 2048².
```

**Correct modifier order**
```text
Sort the modifier stack so Mirror comes before Subdivision on every mesh in Props.
```

### فارسی
می‌توانید تغییر موردنظر را با زبان معمولی توضیح دهید. نمونه‌های زیر نوع کارهای فنی ذکرشده برای Loopcut را نشان می‌دهند؛ نام‌ها و جزئیات را متناسب با صحنه خود تغییر دهید.

**سازمان‌دهی صحنه و ساخت نورپردازی**
```text
همه اشیا را بر اساس ماهیتشان نام‌گذاری کن، چراغ‌ها را در یک Collection جدا قرار بده و اطراف بطری یک چیدمان نور سه‌نقطه‌ای بساز.
```

**اعمال تبدیل‌ها و پاک‌سازی داده‌های هندسی**
```text
مقیاس همه اشیا را اعمال کن، نرمال‌های معکوس را اصلاح کن و داده‌های یتیم را پاک‌سازی کن.
```

**آماده‌سازی ریگ کاراکتر**
```text
برای پاها زنجیره IK همراه با Pole Target بساز و نام‌گذاری دو طرف را به قالب .L و .R تبدیل کن.
```

**هماهنگ‌کردن با تصویر مرجع و آماده‌سازی رندر**
```text
کادربندی را با تصویر مرجعی که پیوست کرده‌ام هماهنگ کن و یک پیش‌تنظیم رندر عکاسی محصول با وضوح 2048² بساز.
```

**اصلاح ترتیب Modifierها**
```text
ترتیب Modifierها را طوری تنظیم کن که در تمام مش‌های داخل Props، گزینه Mirror پیش از Subdivision قرار بگیرد.
```

### 中文
您可以用日常语言描述想要进行的修改。以下示例展示了 Loopcut 文档中列出的技术任务类型；请根据自己的场景调整名称和细节。

**整理场景并创建灯光**
```text
根据每个对象的用途重新命名，把灯光放入单独的集合，并在瓶子周围创建三点布光。
```

**应用变换并清理几何数据**
```text
对所有对象应用缩放，修复翻转的法线，并清理孤立数据。
```

**设置角色绑定**
```text
为腿部添加带极向目标的 IK 链，并将两侧命名统一为 .L/.R 格式。
```

**匹配参考图并准备渲染**
```text
让构图匹配我附上的参考照片，并创建一个分辨率为 2048² 的产品摄影渲染预设。
```

**调整修改器顺序**
```text
调整 Props 集合中每个网格的修改器堆栈，确保 Mirror 排在 Subdivision 之前。
```

---

## How a turn works

### English
Loopcut uses a small set of tools intended to inspect, modify, and verify the Blender scene. The available operations described by the project include:

| Tool | Purpose |
|---|---|
| `run_python` | Runs Python code that changes the scene. The result includes a scene diff measured after execution and may include a viewport capture. |
| `get_scene_info` / `get_object_info` | Reads information about the scene and object setup, including modifiers, materials, geometry-node trees, constraints, and animation. |
| `inspect_api` | Inspects the Python API of the running Blender version and provides tested notes for differences between versions. |
| `capture_viewport` | Captures a view of the scene from a chosen angle and shading style, including information about nearby objects. |
| `compare_with_reference` / `look_at_reference` | Compares an attached reference image with a viewport capture, or inspects a selected region at full resolution. |

The intended workflow is to describe a task, review the proposed code, approve execution, and inspect the resulting scene report. The actual sequence depends on the request and the available model/tool configuration.

You can drop images onto the panel or use **+ image** to attach up to six reference images per message. These images are stored alongside the conversation, not inside your `.blend` file.

### فارسی
Loopcut از مجموعه کوچکی از ابزارها برای بررسی، تغییر و اعتبارسنجی صحنه Blender استفاده می‌کند. عملیات مستندشده در پروژه شامل موارد زیر است:

| ابزار | کاربرد |
|---|---|
| `run_python` | کد Python را برای تغییر صحنه اجرا می‌کند. نتیجه شامل مقایسه تغییرات صحنه پس از اجراست و ممکن است تصویر نمای سه‌بعدی را نیز دربر بگیرد. |
| `get_scene_info` / `get_object_info` | اطلاعات صحنه و تنظیمات اشیا، از جمله Modifierها، متریال‌ها، درخت‌های Geometry Nodes، Constraintها و انیمیشن را می‌خواند. |
| `inspect_api` | API پایتون نسخه در حال اجرای Blender را بررسی می‌کند و برای تفاوت نسخه‌ها اطلاعات آزمایش‌شده ارائه می‌دهد. |
| `capture_viewport` | از صحنه با زاویه و سبک سایه‌زنی انتخاب‌شده تصویر می‌گیرد و اطلاعاتی درباره اشیای نزدیک ارائه می‌کند. |
| `compare_with_reference` / `look_at_reference` | تصویر مرجع پیوست‌شده را با تصویر نمای سه‌بعدی مقایسه می‌کند یا ناحیه‌ای از تصویر را با وضوح کامل بررسی می‌کند. |

گردش‌کار موردنظر این است که وظیفه را توضیح دهید، کد پیشنهادی را بررسی کنید، اجرای آن را تأیید کنید و گزارش نتیجه را ببینید. توالی دقیق مراحل به درخواست شما و مدل و ابزارهای در دسترس بستگی دارد.

برای پیوست‌کردن حداکثر شش تصویر مرجع در هر پیام، تصاویر را روی پنل رها کنید یا از گزینه **+ image** استفاده کنید. این تصاویر کنار گفت‌وگو ذخیره می‌شوند و داخل فایل `.blend` قرار نمی‌گیرند.

### 中文
Loopcut 使用一组精简工具来检查、修改和验证 Blender 场景。项目说明的可用操作包括：

| 工具 | 用途 |
|---|---|
| `run_python` | 运行用于修改场景的 Python 代码。执行结果包含基于实际场景测得的变更差异，也可能附带视口截图。 |
| `get_scene_info` / `get_object_info` | 读取场景和对象设置，包括修改器、材质、几何节点树、约束和动画等信息。 |
| `inspect_api` | 检查当前 Blender 版本的 Python API，并提供经过测试的版本差异说明。 |
| `capture_viewport` | 按指定角度和着色方式捕获场景视图，并提供附近对象的相关信息。 |
| `compare_with_reference` / `look_at_reference` | 将附加的参考图与视口截图进行比较，或以完整分辨率检查图像中的指定区域。 |

预期工作流程是：描述任务、检查建议代码、批准执行，然后查看场景变更报告。实际步骤会根据任务需求以及可用模型和工具配置而有所不同。

您可以将图片拖放到面板中，或使用 **+ image**，每条消息最多附加六张参考图片。这些图片会与对话一起保存，而不会存入您的 `.blend` 文件。

---

## Privacy and conversation history

### English
Loopcut conversations are associated with the Blender file they were used with. **History** lists previous conversations, and **New chat** starts a new one. For long sessions, older steps may be folded and summarized to help keep the displayed context within budget.

The project describes a text-only conversation log retained for 90 days to help troubleshoot issues and improve the app. According to that description, the log does not include images, `.blend` files, or API keys and is not used for training. You can turn this sharing off using **Share conversations to improve Loopcut** under **Preferences › Add-ons › Loopcut › Privacy and Support**. The **Report a Problem…** action in that area can send a report and, if you choose, recent conversations; it provides a code you can quote when following up.

These statements reflect the project documentation and may change between releases. Review the current in-app privacy settings and repository documentation before sharing sensitive work.

### فارسی
گفت‌وگوهای Loopcut به فایل Blender مربوط به همان کار وابسته‌اند. بخش **History** گفت‌وگوهای قبلی را نمایش می‌دهد و **New chat** یک گفت‌وگوی جدید آغاز می‌کند. در نشست‌های طولانی، ممکن است مراحل قدیمی‌تر جمع‌بندی شوند تا حجم اطلاعات نمایش‌داده‌شده در محدوده مناسب باقی بماند.

طبق توضیحات پروژه، برای رفع اشکال و بهبود برنامه، گزارش متنی گفت‌وگوها به مدت ۹۰ روز نگه‌داری می‌شود. بر اساس همین توضیحات، این گزارش شامل تصاویر، فایل‌های `.blend` یا کلیدهای API نیست و برای آموزش مدل استفاده نمی‌شود. برای غیرفعال‌کردن این اشتراک‌گذاری، در مسیر **Preferences › Add-ons › Loopcut › Privacy and Support** گزینه **Share conversations to improve Loopcut** را خاموش کنید. گزینه **Report a Problem…** در همان بخش می‌تواند گزارشی ارسال کند و در صورت انتخاب شما، گفت‌وگوهای اخیر را نیز ضمیمه کند؛ سپس کدی برای پیگیری در اختیار شما می‌گذارد.

این موارد بر اساس مستندات پروژه بیان شده‌اند و ممکن است در نسخه‌های بعدی تغییر کنند. پیش از ارسال اطلاعات حساس، تنظیمات حریم خصوصی داخل برنامه و مستندات فعلی مخزن را بررسی کنید.

### 中文
Loopcut 对话与其所处理的 Blender 文件相关联。**History** 会列出以前的对话，**New chat** 则会开始新对话。对于较长的会话，较早的步骤可能会被折叠并总结，以便将显示的上下文控制在合理范围内。

项目说明称，为了排查问题和改进应用，文本形式的对话日志会保留 90 天。根据该说明，日志不包含图片、`.blend` 文件或 API 密钥，也不会用于模型训练。您可以在 **Preferences › Add-ons › Loopcut › Privacy and Support** 中关闭 **Share conversations to improve Loopcut**。同一位置的 **Report a Problem…** 可以发送问题报告；如果您选择，也可以附上最近的对话，并获得一个用于后续沟通的编号。

以上内容依据项目文档整理，可能会随版本更新而变化。分享敏感项目资料之前，请检查应用内当前的隐私设置和仓库文档。

---

## Building from source

### English
Loopcut is described as a fork of [Blender](https://projects.blender.org/blender/blender) 5.2.2 on the `main` branch. The Loopcut add-on is located at `scripts/addons_core/loopcut/` and supports hot reloading. The fork adds an editor type, in-place snapshot restoration, a separate settings directory, and its own product name and icons.

The commands documented for the development workflow are:

```bash
make update
# Fetch Blender's libraries from projects.blender.org

ninja -C ../build/lite install
# Build/install the development version; this also re-copies the add-on after Python-only changes

python3 -m unittest discover -s loopcut/tests
# Run the Loopcut Python unit tests
```

Run build commands from the appropriate source/build directory and ensure Blender's required dependencies and development environment are installed. The [developer guide](loopcut/DEVELOPING.md) describes the repository layout, development loop, test harness and evaluation suite, releases, checkpoints, conversations, and context management.

### فارسی
طبق توضیحات پروژه، Loopcut شاخه‌ای از [Blender](https://projects.blender.org/blender/blender) نسخه 5.2.2 و بر پایه شاخه `main` است. افزونه Loopcut در مسیر `scripts/addons_core/loopcut/` قرار دارد و از بارگذاری مجدد در زمان اجرا (hot reload) پشتیبانی می‌کند. این شاخه یک نوع ویرایشگر، بازیابی درجا از snapshot، پوشه تنظیمات جداگانه و نام و نمادهای اختصاصی محصول را اضافه می‌کند.

دستورهای مستندشده برای گردش‌کار توسعه عبارت‌اند از:

```bash
make update
# دریافت کتابخانه‌های Blender از projects.blender.org

ninja -C ../build/lite install
# ساخت/نصب نسخه توسعه؛ پس از تغییرات صرفاً پایتونی، افزونه را دوباره کپی می‌کند

python3 -m unittest discover -s loopcut/tests
# اجرای آزمون‌های واحد Python مربوط به Loopcut
```

دستورهای ساخت را از مسیر صحیح سورس/ساخت اجرا کنید و مطمئن شوید وابستگی‌های لازم Blender و محیط توسعه نصب شده‌اند. [راهنمای توسعه](loopcut/DEVELOPING.md) ساختار مخزن، چرخه توسعه، ابزارهای آزمون و ارزیابی، انتشار نسخه‌ها، نقاط بازیابی، گفت‌وگوها و مدیریت زمینه را توضیح می‌دهد.

### 中文
项目将 Loopcut 描述为基于 `main` 分支的 [Blender](https://projects.blender.org/blender/blender) 5.2.2 分支版本。Loopcut 扩展位于 `scripts/addons_core/loopcut/`，并支持热重载。该分支增加了一种编辑器类型、原位快照恢复、独立设置目录，以及专属的产品名称和图标。

项目文档列出的开发命令如下：

```bash
make update
# 从 projects.blender.org 获取 Blender 所需的库

ninja -C ../build/lite install
# 构建/安装开发版本；仅修改 Python 代码后也会重新复制扩展

python3 -m unittest discover -s loopcut/tests
# 运行 Loopcut 的 Python 单元测试
```

请在正确的源代码/构建目录中执行构建命令，并确保已安装 Blender 所需依赖和开发环境。[开发指南](loopcut/DEVELOPING.md) 介绍仓库结构、开发循环、测试框架与评估套件、版本发布、检查点、对话以及上下文管理。

---

## Contributing

### English
Bug reports, issues, and pull requests are welcome. The documented rapid development loop uses `loopcut/scripts/dev.sh`: Blender remains open, and saving a file reloads the panel. The command `python3 -m unittest discover -s loopcut/tests` runs the tests without requiring Blender to be open. The project states that Blender-free tests run on every push.

Before submitting a change, describe the intended behavior, keep changes focused, run the relevant tests where your environment permits, and include reproduction steps for bug reports. Consult the developer guide for project-specific contribution and testing details.

### فارسی
گزارش باگ، ثبت Issue و ارسال Pull Request مورد استقبال است. چرخه سریع توسعه مستندشده از `loopcut/scripts/dev.sh` استفاده می‌کند: Blender باز می‌ماند و با ذخیره فایل، پنل دوباره بارگذاری می‌شود. دستور `python3 -m unittest discover -s loopcut/tests` آزمون‌ها را بدون نیاز به بازبودن Blender اجرا می‌کند. طبق توضیحات پروژه، آزمون‌هایی که به Blender نیاز ندارند با هر push اجرا می‌شوند.

پیش از ارسال تغییر، رفتار موردنظر را روشن توضیح دهید، تغییرات را تا حد امکان محدود و متمرکز نگه دارید، آزمون‌های مرتبط را در صورت آماده‌بودن محیط اجرا کنید و برای گزارش خطا مراحل بازتولید را بنویسید. برای جزئیات مشارکت و آزمون‌های اختصاصی پروژه، راهنمای توسعه را مطالعه کنید.

### 中文
欢迎提交错误报告、Issue 和 Pull Request。文档所述的快速开发流程使用 `loopcut/scripts/dev.sh`：Blender 保持打开状态，保存文件后面板会重新加载。命令 `python3 -m unittest discover -s loopcut/tests` 可以在不打开 Blender 的情况下运行测试。项目说明称，每次推送代码时都会运行无需 Blender 的测试。

提交更改前，请清楚描述预期行为，尽量保持修改范围集中，在环境允许的情况下运行相关测试，并在错误报告中提供复现步骤。有关项目专属的贡献和测试要求，请参阅开发指南。

---

## Bundled add-ons

### English
Loopcut includes optional System extensions that are shipped unmodified and remain disabled until needed. Their upstream authors and licenses should continue to be credited:

- [UniV](https://extensions.blender.org/add-ons/univ/) by Oxicid — GPL-3.0-or-later.
- [LoopTools](https://extensions.blender.org/add-ons/looptools/) by Bart Crouch and Vladimir Spivak, maintained by the community — GPL-2.0-or-later.
- [Node Arrange](https://extensions.blender.org/add-ons/node-arrange/) maintained by Leonardo Pike-Excell — GPL-3.0-or-later; bundled NetworkX is under BSD-3-Clause.
- [MPFB](https://extensions.blender.org/add-ons/mpfb/) maintained by Joel Palmius and the MakeHuman community — code under GPL-3.0-or-later; included assets under CC0 1.0. Additional asset packs are not bundled.
- [Bool Tool](https://extensions.blender.org/add-ons/bool-tool/) maintained by Nika Kutsniashvili and upstream contributors — GPL-3.0-or-later.

Pinned versions and full credits are recorded in [`bundled.json`](release/extensions/bundled.json). License texts are available under [`release/extensions/licenses/`](release/extensions/licenses/), and shipped Python sources are in [`release/extensions/system/`](release/extensions/system/). The project states that these packages contain no compiled components; the bundled NetworkX wheel used by Node Arrange is pure Python.

### فارسی
Loopcut شامل افزونه‌های اختیاری System است که بدون تغییر همراه پروژه عرضه می‌شوند و تا زمان نیاز غیرفعال باقی می‌مانند. نام سازندگان اصلی و مجوزهای آن‌ها باید حفظ و ذکر شود:

- [UniV](https://extensions.blender.org/add-ons/univ/) اثر Oxicid — مجوز GPL-3.0-or-later.
- [LoopTools](https://extensions.blender.org/add-ons/looptools/) اثر Bart Crouch و Vladimir Spivak، با نگه‌داری جامعه کاربری — مجوز GPL-2.0-or-later.
- [Node Arrange](https://extensions.blender.org/add-ons/node-arrange/) با نگه‌داری Leonardo Pike-Excell — مجوز GPL-3.0-or-later؛ بسته NetworkX همراه آن تحت BSD-3-Clause است.
- [MPFB](https://extensions.blender.org/add-ons/mpfb/) با نگه‌داری Joel Palmius و جامعه MakeHuman — کد تحت GPL-3.0-or-later و دارایی‌های همراه تحت CC0 1.0 هستند. بسته‌های دارایی اضافی همراه پروژه نیستند.
- [Bool Tool](https://extensions.blender.org/add-ons/bool-tool/) با نگه‌داری Nika Kutsniashvili و مشارکت‌کنندگان بالادستی — مجوز GPL-3.0-or-later.

نسخه‌های دقیق و اطلاعات کامل انتساب در فایل [`bundled.json`](release/extensions/bundled.json) ثبت شده‌اند. متن مجوزها در مسیر [`release/extensions/licenses/`](release/extensions/licenses/) و کدهای Python همراه در [`release/extensions/system/`](release/extensions/system/) قرار دارند. طبق توضیحات پروژه، این بسته‌ها اجزای کامپایل‌شده ندارند و بسته NetworkX همراه Node Arrange کاملاً از Python تشکیل شده است.

### 中文
Loopcut 包含可选的 System 扩展，这些扩展以未修改的形式随项目提供，并在需要时才启用。应继续注明其上游作者和许可证：

- [UniV](https://extensions.blender.org/add-ons/univ/) 作者 Oxicid — GPL-3.0-or-later。
- [LoopTools](https://extensions.blender.org/add-ons/looptools/) 作者 Bart Crouch 和 Vladimir Spivak，由社区维护 — GPL-2.0-or-later。
- [Node Arrange](https://extensions.blender.org/add-ons/node-arrange/) 由 Leonardo Pike-Excell 维护 — GPL-3.0-or-later；随附的 NetworkX 使用 BSD-3-Clause。
- [MPFB](https://extensions.blender.org/add-ons/mpfb/) 由 Joel Palmius 和 MakeHuman 社区维护 — 代码使用 GPL-3.0-or-later，随附资源使用 CC0 1.0；项目不包含额外资源包。
- [Bool Tool](https://extensions.blender.org/add-ons/bool-tool/) 由 Nika Kutsniashvili 及上游贡献者维护 — GPL-3.0-or-later。

固定版本和完整致谢记录在 [`bundled.json`](release/extensions/bundled.json) 中。许可证文本位于 [`release/extensions/licenses/`](release/extensions/licenses/)，随附的 Python 源码位于 [`release/extensions/system/`](release/extensions/system/)。项目说明称，这些软件包不包含编译后的组件；Node Arrange 随附的 NetworkX wheel 仅包含纯 Python 代码。

---

## License and name

### English
The project describes its code as a combination of Blender code and Loopcut changes, distributed under the GNU General Public License version 3 or later, like Blender. The full license text is in [`LICENSE`](LICENSE); related license and documentation files include [`COPYING`](COPYING) and [`doc/license/`](doc/license/). This also applies to the add-on, which is written against Blender's Python API and ships inside the application. The hosted model service is separate work maintained in its own repository.

The license applies to code; it does not grant permission to use the Loopcut product name or mark. “Loopcut” and its mark, located in [`release/loopcut/`](release/loopcut/), identify this product. A fork of this repository should use its own name and icons. Blender is a trademark of the Blender Foundation. Loopcut is based on Blender and is not affiliated with or endorsed by the Blender Foundation.

**Project developer and maintainer / توسعه‌دهنده و نگه‌دارنده پروژه / 项目开发者与维护者:** Hamid Yarali（حمید یارعلی）  
**Repository / مخزن / 仓库:** https://github.com/HamidYaraliOfficial/Loopcut

### فارسی
طبق توضیحات پروژه، کد این محصول ترکیبی از کد Blender و تغییرات Loopcut است و مانند Blender تحت مجوز GNU General Public License نسخه ۳ یا نسخه‌های بعدی منتشر می‌شود. متن کامل مجوز در فایل [`LICENSE`](LICENSE) قرار دارد؛ فایل‌های مرتبط شامل [`COPYING`](COPYING) و مسیر [`doc/license/`](doc/license/) هستند. این مجوز افزونه را نیز دربر می‌گیرد؛ افزونه با API پایتون Blender نوشته شده و همراه برنامه عرضه می‌شود. سرویس مدل میزبانی‌شده پروژه‌ای جداگانه است که در مخزن مستقل خود نگه‌داری می‌شود.

مجوز کد به‌خودی‌خود اجازه استفاده از نام محصول یا نشان Loopcut را نمی‌دهد. نام «Loopcut» و نشان آن که در مسیر [`release/loopcut/`](release/loopcut/) قرار دارند، هویت این محصول را مشخص می‌کنند. شاخه‌های مشتق‌شده از این مخزن باید از نام و نمادهای مخصوص خود استفاده کنند. Blender علامت تجاری Blender Foundation است. Loopcut بر پایه Blender ساخته شده و وابسته به Blender Foundation نیست و مورد تأیید رسمی آن نیز قرار ندارد.

**توسعه‌دهنده و نگه‌دارنده پروژه:** حمید یارعلی (Hamid Yarali)  
**مخزن گیت‌هاب:** https://github.com/HamidYaraliOfficial/Loopcut

### 中文
项目说明称，该项目的代码由 Blender 代码与 Loopcut 修改组成，并与 Blender 一样依据 GNU 通用公共许可证第 3 版或更高版本发布。完整许可证文本位于 [`LICENSE`](LICENSE)；相关文件还包括 [`COPYING`](COPYING) 和 [`doc/license/`](doc/license/)。该许可证也适用于随应用一同发布、基于 Blender Python API 编写的扩展。托管模型服务属于独立项目，并在其自己的仓库中维护。

该许可证适用于代码，但并不自动授予使用 Loopcut 产品名称或标志的权利。“Loopcut”名称及其标志位于 [`release/loopcut/`](release/loopcut/)，用于识别本产品。本仓库的分支或衍生项目应使用自己的名称和图标。Blender 是 Blender Foundation 的商标。Loopcut 基于 Blender 构建，但与 Blender Foundation 没有隶属关系，也未获得其认可或背书。

**项目开发者与维护者：** Hamid Yarali（حمید یارعلی）  
**GitHub 仓库：** https://github.com/HamidYaraliOfficial/Loopcut

---

<p align="center">
  **فارسی:** این مستند برای معرفی Loopcut به سه زبان انگلیسی، فارسی و چینی تهیه شده است. برای دریافت نسخه‌ها، گزارش مشکل و مشاهده تغییرات، از مخزن گیت‌هاب پروژه استفاده کنید.
  <br>
  **English:** This README introduces Loopcut in English, Persian, and Chinese. Use the project repository to obtain releases, report issues, and review changes.
  <br>
  **中文：** 本 README 使用英语、波斯语和中文介绍 Loopcut。请通过项目仓库获取发布版本、报告问题并查看变更。
  <br><br>
  <a href="https://github.com/HamidYaraliOfficial/Loopcut">HamidYaraliOfficial/Loopcut</a>
</p>
