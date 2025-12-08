## CAVE PC Shmups BGM Replace Tool ｜ CAVE PC 射击音频替换工具

[English](#english) · [中文](#中文)

### English

**Goal**  
Replace or extract BGM/SE audio for CAVE PC releases (e.g., Dai-Fukkatsu, Deathsmiles) by reading their packed sound archives and writing them back with modified WAVs.

**Features**
- Parse game archives and list contained WAV entries.
- Preview selected entry via built-in player.
- Export one or all WAVs.
- Replace a WAV with your own file and save a new archive.
- Handles both big-endian and little-endian layouts for supported titles.

**Supported modes (selector options)**
- Dai-Fukkatsu (big-endian)
- Deathsmiles (little-endian)
- Deathsmiles I・II Type A (`Stream.bin`)
- Deathsmiles I・II Type B (`Sound.bin`)

**Requirements**
- Windows with .NET Framework 4.8
- Visual Studio 2019+ (or `msbuild`) to build

**Build**
1) Open `WavReplace.sln` in Visual Studio.  
2) Select `Release` and build.  
3) The executable is produced at `WavReplace\bin\Release\WavReplace.exe`.

**Usage**
1) Launch `WavReplace.exe`.  
2) Choose game type from the dropdown (top-right).  
3) Click “选择文件” to load the game archive (e.g., `Stream.bin` / `Sound.bin` / main data file). The list shows detected WAV entries.  
4) Select an entry to preview; use “保存选中文件” to export it, or “提取所有文件” to batch-export.  
5) Click the lower “选择文件” to pick a replacement WAV, then “以选择文件替换上方选中文件” to swap it in.  
6) After replacements, click “保存修改” and choose where to save the rebuilt archive.  
7) Optionally use “播放/停止” to audition the current selection.

**Notes**
- Keep replacement audio as WAV; the tool writes raw bytes without format conversion.
- Offsets are recalculated automatically before saving; ensure the game is not running when you overwrite files.

**Links**
- Source tree: `WavReplace/`  
- Prebuilt/Release (if available): https://github.com/<owner>/PC_Cave_Shumps_BGM_Replace_Tool/releases

---

### 中文

**目的**  
用于 PC 端 CAVE 射击游戏（如《大复活》《死笑》）的 BGM/音效打包文件解析、提取与 WAV 替换。

**功能**
- 解析音频包，列出其中的 WAV 条目。
- 内置预听：选中即可播放。
- 导出单个或全部 WAV。
- 选择本地 WAV 进行替换并重写音频包。
- 同时支持大端/小端格式的已知版本。

**支持的模式（下拉框选项）**
- 大复活（大端数据）
- 死笑（小端数据）
- 死笑 I·II Type A（`Stream.bin`）
- 死笑 I·II Type B（`Sound.bin`）

**环境要求**
- Windows，已安装 .NET Framework 4.8
- Visual Studio 2019+（或使用 `msbuild`）进行编译

**编译步骤**
1) 用 Visual Studio 打开 `WavReplace.sln`。  
2) 选择 `Release` 配置并构建。  
3) 可执行文件生成于 `WavReplace\bin\Release\WavReplace.exe`。

**使用步骤**
1) 运行 `WavReplace.exe`。  
2) 在右上方下拉框选择对应游戏模式。  
3) 点击上方“选择文件”载入游戏音频包（如 `Stream.bin`/`Sound.bin`/主数据文件），列表会显示所有 WAV。  
4) 选中条目即可预听；用“保存选中文件”导出单个，或“提取所有文件”批量导出。  
5) 点击下方“选择文件”挑选替换用的 WAV，然后“以选择文件替换上方选中文件”完成替换。  
6) 全部替换完成后点“保存修改”，选择输出路径保存新的音频包。  
7) 可用“播放/停止”按钮随时试听当前选中项。

**注意**
- 请使用 WAV 文件进行替换，工具不会转换格式。  
- 保存前会自动重算偏移，覆盖游戏文件前请关闭游戏。

**相关链接**
- 源码目录：`WavReplace/`  
- 若有发布包： https://github.com/<owner>/PC_Cave_Shumps_BGM_Replace_Tool/releases

