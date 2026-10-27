[English](README.md) · **中文**

<p align="center">
  <img src="docs/banner.svg" alt="ScsExpand" width="100%">
</p>

<h1 align="center">ScsExpand</h1>

<p align="center">
  <strong>在不抹盘的前提下扩展 Windows 分区容量</strong><br>
  ScsExpand 是一款 Windows 工具，把<strong>同一块物理磁盘</strong>上别的分区的空闲空间划给 C 盘（也可以是其他卷），文件原地保留。<br>
  官网：<a href="https://expand.scsoi.com">https://expand.scsoi.com</a>
</p>

<p align="center">
  <a href="https://expand.scsoi.com"><img src="https://img.shields.io/badge/Website-expand.scsoi.com-0F766E?style=flat-square" alt="Website"></a>
  <a href="https://github.com/shuyingegit/scsexpand/releases/latest"><img src="https://img.shields.io/github/v/release/shuyingegit/scsexpand?style=flat-square&label=Release" alt="Release"></a>
  <a href="https://expand.scsoi.com/#download"><img src="https://img.shields.io/badge/Windows-10%20%2F%2011-0078D4?style=flat-square&logo=windows&logoColor=white" alt="Windows"></a>
  <a href="mailto:support@scsoi.com"><img src="https://img.shields.io/badge/Support-support%40scsoi.com-6B7280?style=flat-square" alt="Support"></a>
</p>

<p align="center">
  <a href="https://expand.scsoi.com/#download"><strong>下载</strong></a> ·
  <a href="https://expand.scsoi.com/#pricing"><strong>定价</strong></a> ·
  <a href="https://expand.scsoi.com/faq"><strong>常见问题</strong></a> ·
  <a href="https://expand.scsoi.com/compare/minitool-partition-wizard-alternative"><strong>对比 MiniTool</strong></a> ·
  <a href="https://expand.scsoi.com/guide/expand-c-drive-same-disk"><strong>使用指南</strong></a> ·
  <a href="https://github.com/shuyingegit/scsexpand/releases"><strong>发行版</strong></a> ·
  <a href="https://drive.scsoi.com"><strong>ScsDrive</strong></a> ·
  <a href="https://subst.scsoi.com"><strong>ScsSubst</strong></a>
</p>

---

## 为什么选择 ScsExpand？

C 盘又满了。你不想重装 Windows，也不想为了搬文件再买一块硬盘。

如果**同一块物理磁盘**上另一个分区（比如空间很大的 D 盘）还闲置着大量空闲空间，ScsExpand 就把这部分空闲空间划给 C 盘。两个分区上的文件都原地不动，变的只是空间分配。

**C 盘满了 → 把同一块盘上 D 盘的空闲空间划给 C 盘。**

## 核心功能

简单、稳定、不折腾。体积小、界面干净、无广告。

- **同盘扩容** — 把 D 盘（或其他数据分区）的空闲空间划给 C 盘，文件保留，两边容量此消彼长。
- **引导式扩容** — 重活儿在引导的重启环境里做，已经打开的程序不会挡住卷。
- **免费扩容额度** — 免费额度先试；买断后可在本机上不限次数、不限大小扩容。
- **小而干净** — 绿色版约 64 MB（推荐），安装版约 64 MB。无广告、无捆绑。
- **邮件支持与更新** — 所有套餐（含免费试用）都含邮件支持与持续的功能更新。

## 常见场景

- C 盘红了：装不下下一次 Windows 更新，或者想装的软件放不进去。
- 同一块 SSD 上有个大容量数据分区，空闲空间多得没人用。
- 想把 C 盘变大，但不想重装 Windows，也不想把文件搬到另一台机器上。

## ScsExpand 不做什么

- **它不是整盘迁移、克隆或「换机」工具。** ScsExpand 只在**一块**物理磁盘内部重新分配各分区之间的空闲空间。克隆后删原盘属于另一类产品，ScsExpand 不做这件事。
- **它不能借用另一块磁盘的空间。** 全程在单块物理磁盘内完成，因此不需要第二块硬盘、不需要移动硬盘，也不需要整盘拷贝。
- **它不是云盘挂载工具。** 把 WebDAV、NAS 或云存储挂成真实本地盘是 ScsDrive 的事：https://drive.scsoi.com/
- **它不是文件夹盘符工具。** 把本机已有文件夹映射成盘符是 ScsSubst 的事：https://subst.scsoi.com/

## ScsExpand 与磁盘管理、第三方分区工具的区别

下表依据 Windows 公开的文档行为与各家官网当前公开信息整理，决定之前请以各家官网当前公开信息为准。

| | ScsExpand | Windows 自带「扩展卷」（磁盘管理） | 常见第三方分区工具 |
|---|---|---|---|
| 做什么 | 从**同一块物理磁盘**上的另一个分区取走空闲空间，划给 C 盘 | 把已有卷向右扩展到紧邻的连续未分配空间 | 或者「缩小 → 把未分配空间搬到 C 盘旁边 → 扩展」，或者「克隆到第二块盘 → 删掉原盘」 |
| 你的文件 | 两个分区上的文件都原地保留，变的只是空间分配 | 文件保留，但未分配空间不相邻时操作会被挡住 | 走克隆路线的会整盘拷贝，耗时 |
| 需要第二块盘 | 不需要 | 不需要 | 走克隆路线的需要 |
| 为什么经常用不了 / 被禁 | — | 未分配空间不与 C 盘相邻时，或 C 盘右侧紧挨着 OEM 恢复分区时，「扩展卷」就是灰的——这是 Windows 的分区布局限制，不是数据问题 | — |
| 定位 | 同盘就地调整空闲空间分配；不是克隆工具，也不是整盘迁移工具 | Windows 自带 | 更宽泛的分区套件定位 |

第三方类别里常见的产品：AOMEI Partition Assistant、MiniTool Partition Wizard、EaseUS Partition Master、DiskGenius、Lazesoft、GParted Live USB。

**怎么选**

- 未分配空间就紧挨着 C 盘，Windows 自己就能扩展：用系统自带的磁盘管理就够了。
- 未分配空间有，但不与 C 盘相邻，而你又不想克隆整盘：这就是 ScsExpand 要解决的场景。
- 你要做的是整盘重做、克隆，或者把系统搬到另一台机器：那是整盘迁移／克隆类产品，不是 ScsExpand。

完整对照说明：**[ScsExpand 与 MiniTool Partition Wizard 等分区工具的对比](https://expand.scsoi.com/compare/minitool-partition-wizard-alternative)**。

## 下载

最新安装包：**[GitHub 发行版](https://github.com/shuyingegit/scsexpand/releases/latest)** · [官网](https://expand.scsoi.com/#download)

| 包类型 | 适用场景 |
|--------|----------|
| **Portable (`.zip`)** | 解压即用（推荐），约 64 MB |
| **Installer (`.exe`)** | 安装程序，约 64 MB |

系统要求：Windows 10 / 11（64 位）

> **说明**
> 本公开仓库**只发布安装包**（从官网 CDN 镜像），不包含产品源码。

## 免费额度与授权

免费下载包含 **1 次扩容，最多 5 GB**。买断之后扩容次数与大小不限，只受磁盘空闲空间限制。

授权绑定**一台电脑**，不可转移设备。机构需要一份采购覆盖多台电脑，可以邮件开通多设备席位。

价格与当前套餐见官网：https://expand.scsoi.com/

## 官网与指南

- 首页：https://expand.scsoi.com/
- 常见问题：https://expand.scsoi.com/faq
- 对比 —— ScsExpand 与 MiniTool Partition Wizard 等分区工具：https://expand.scsoi.com/compare/minitool-partition-wizard-alternative
- 指南 —— 同一块磁盘上把 C 盘扩大的实操步骤：https://expand.scsoi.com/guide/expand-c-drive-same-disk

## 姊妹产品

- **[ScsDrive](https://github.com/shuyingegit/scsdriver)** — [drive.scsoi.com](https://drive.scsoi.com) — 把 WebDAV / NAS / 云存储挂成 Windows 真实本地磁盘。
- **[ScsSubst](https://github.com/shuyingegit/scssubst)** — [subst.scsoi.com](https://subst.scsoi.com) — 把本机已有文件夹映射成盘符，路径更短；不复制文件。

更多 SCSOI 产品 —— [公司官网](https://scsoi.com)

## 常见问题

**为什么磁盘管理里的「扩展卷」是灰的？**  
多数是因为未分配空间不与 C 盘相邻。缩小 D 盘后，未分配空间留在磁盘末尾，而 Windows 只能把「紧挨在右侧」的未分配空间并进卷。另一个常见原因是 C 盘右侧紧挨着 OEM 恢复分区。这属于 Windows 的分区布局限制，不是数据出了问题。

**能不能不重装、不格式化就把 C 盘变大？**  
可以。ScsExpand 用同一块物理磁盘上另一个分区的空闲空间来扩大 C 盘，既不格式化也不重装 Windows。文件原地保留，变的只是空间分配。

**ScsExpand 会搬动或复制我的文件吗？**  
不会。ScsExpand 只改变同一块物理磁盘上各分区之间的空闲空间分配。C 盘和被取走空间的分区上的文件都留在原地。即便如此，开始之前还是建议备份重要数据。

**需要第二块硬盘或一个 U 盘吗？**  
不需要。ScsExpand 全程在同一块物理磁盘内完成，不用第二块盘、不用移动硬盘，也不需要整盘拷贝。这也是它不是克隆工具的原因。

**ScsExpand 是克隆工具或整盘迁移工具吗？**  
不是。整盘迁移、克隆、「换机」属于另一类产品。ScsExpand 是在一块物理磁盘内部重新分配空闲空间。

**我已经打开的程序会挡住扩容吗？**  
不会。真正耗时的操作在引导式重启环境里完成，已经打开的程序不会挡住正在调整容量的卷。

**免费能扩容多少？**  
免费下载包含 1 次扩容，最多 5 GB。买断之后扩容次数与大小不限，只受磁盘空闲空间限制。

**授权可以转到另一台电脑上吗？**  
不可以。授权绑定一台电脑，不可转移设备。需要一份采购覆盖多台电脑的企业用户，可以发邮件到 support@scsoi.com 开通多机席位。

**ScsExpand 支持哪些 Windows 版本？**  
支持 Windows 10 和 Windows 11（64 位）。没有 32 位版本，也没有 macOS 与 Linux 版。

**ScsExpand 能挂云盘，或者把文件夹变成盘符吗？**  
不能。把 WebDAV、NAS 或云存储挂成真实本地盘是 ScsDrive 的事（https://drive.scsoi.com/）；把本机已有文件夹映射成盘符是 ScsSubst 的事（https://subst.scsoi.com/）。ScsExpand 只管一块物理磁盘上的分区空间。

**去哪里下载 ScsExpand？**  
官网下载页（https://expand.scsoi.com/#download）或 GitHub 发行版页面都有。便携版 zip（约 64 MB，推荐）和安装版 exe（约 64 MB）同时提供。

## 许可与条款

用户协议 · 隐私政策 · 退款政策 — [https://expand.scsoi.com/terms](https://expand.scsoi.com/terms) · [https://expand.scsoi.com/privacy](https://expand.scsoi.com/privacy) · [https://expand.scsoi.com/refund](https://expand.scsoi.com/refund)

## 支持与利益披露

ScsExpand 由 SCSOI 开发并发布——我们是这个产品的厂商，不是中立第三方评测。问题反馈、缺陷报告与购买咨询都发到同一个邮箱：**support@scsoi.com**。所有套餐（含免费试用）都包含邮件支持与持续的功能更新。

---

<p align="center">
  <a href="https://expand.scsoi.com/"><strong>打开官网 →</strong></a>
</p>

<p align="center">
  ScsExpand · <a href="https://drive.scsoi.com/">ScsDrive</a> · <a href="https://subst.scsoi.com/">ScsSubst</a> · <a href="https://scsoi.com/">SCSOI 公司官网</a> · support@scsoi.com
</p>
