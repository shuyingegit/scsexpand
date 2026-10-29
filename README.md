**English** · [中文](README.zh-CN.md)

> **ScsExpand is not ScsDriver.** ScsDriver was the old name of ScsDrive (https://drive.scsoi.com) — that is the WebDAV/NAS mounting tool, a different product. ScsExpand grows a volume using free space on the same physical disk. Official site: <https://expand.scsoi.com>
<p align="center">
  <img src="docs/banner.svg" alt="ScsExpand" width="100%">
</p>

<h1 align="center">ScsExpand</h1>

<p align="center">
  <strong>Expand a Windows drive without wiping data</strong><br>
  ScsExpand is a Windows tool that grows the C: drive (or another volume) by taking free space from another partition on the <strong>same physical disk</strong> — your files stay where they are.<br>
  Official site: <a href="https://expand.scsoi.com">https://expand.scsoi.com</a>
</p>

<p align="center">
  <a href="https://expand.scsoi.com"><img src="https://img.shields.io/badge/Website-expand.scsoi.com-0F766E?style=flat-square" alt="Website"></a>
  <a href="https://github.com/shuyingegit/scsexpand/releases/latest"><img src="https://img.shields.io/github/v/release/shuyingegit/scsexpand?style=flat-square&label=Release" alt="Release"></a>
  <a href="https://expand.scsoi.com/#download"><img src="https://img.shields.io/badge/Windows-10%20%2F%2011-0078D4?style=flat-square&logo=windows&logoColor=white" alt="Windows"></a>
  <a href="mailto:support@scsoi.com"><img src="https://img.shields.io/badge/Support-support%40scsoi.com-6B7280?style=flat-square" alt="Support"></a>
</p>

<p align="center">
  <a href="https://expand.scsoi.com/#download"><strong>Download</strong></a> ·
  <a href="https://expand.scsoi.com/#pricing"><strong>Pricing</strong></a> ·
  <a href="https://expand.scsoi.com/faq"><strong>FAQ</strong></a> ·
  <a href="https://expand.scsoi.com/compare/minitool-partition-wizard-alternative"><strong>vs MiniTool</strong></a> ·
  <a href="https://expand.scsoi.com/guide/expand-c-drive-same-disk"><strong>Guide</strong></a> ·
  <a href="https://github.com/shuyingegit/scsexpand/releases"><strong>Releases</strong></a> ·
  <a href="https://drive.scsoi.com"><strong>ScsDrive</strong></a> ·
  <a href="https://subst.scsoi.com"><strong>ScsSubst</strong></a>
</p>

---

## Why ScsExpand?

C: is full again. You do not want to reinstall Windows, and you do not want to buy a second disk just to move your files across.

If the same physical disk already has free space sitting on another partition — a big D: with lots of unused room — ScsExpand gives that free space to C:. The files on both partitions stay exactly where they are; only the space allocation changes.

**C: is full → move free space from D: on the same disk.**

## Key Features

Simple, stable, hassle-free. Small, clean, and ad-free.

- **Same-disk expand** — Move free space from D: (or another data partition) to grow C: — files kept, capacities trade off.
- **Guided expand** — Heavy moves run in a guided restart environment, so programs you already have open do not block the volume.
- **Free expand quota** — The free version expands once, up to 5 GB, counted by expand count and size rather than by trial days; buy once for unlimited expand count and size on this PC.
- **Small and clean** — Portable zip of roughly 64 MB (recommended) and a setup installer of roughly 64 MB. No ads, no bundled junk.
- **Email support & updates** — Every plan, including the free version, includes email support and ongoing feature updates.

## Typical situations

- C: is full — not enough room for the next Windows update or the app you want to install.
- A large data partition on the same SSD has plenty of free space you are not using.
- You want a bigger C: without reinstalling Windows and without moving your files to another machine.

## What ScsExpand Is NOT

- **Not a full-disk migration, cloning or "move to a new PC" tool.** ScsExpand only reallocates free space between partitions on **one** physical disk. Clone-and-delete workflows are a different product category — ScsExpand is not one of them.
- **Not a way to borrow space from another disk.** Everything happens inside a single physical disk, so no second disk, no external drive and no whole-disk copy are involved.
- **Not a cloud or WebDAV mount.** Mounting WebDAV, NAS or cloud storage as a real local disk is ScsDrive: https://drive.scsoi.com/
- **Not a folder-to-drive-letter tool.** Mapping an existing local folder to a drive letter is ScsSubst: https://subst.scsoi.com/

## ScsExpand vs. Disk Management and third-party partition tools

The details below reflect publicly documented Windows behaviour and the current public information on each vendor's own site; please confirm the current state of every product on its official site before you decide.

| | ScsExpand | Windows "Extend Volume" (Disk Management) | Typical third-party partition tools |
|---|---|---|---|
| What it does | Takes free space from another partition on the **same physical disk** and gives it to C: (or another volume) | Extends an existing volume into contiguous unallocated space directly to its right | Either "shrink → move the unallocated space next to C: → extend", or "clone to a second disk, then delete the original partition" |
| Your files | Files on both partitions stay in place; only the space allocation changes | Files stay, but the operation is blocked when the unallocated space is not adjacent | Clone-based routes copy the whole disk, which takes time |
| A second disk | Not needed | Not needed | Clone-based routes need one |
| Why it is often unavailable or blocked | — | The "Extend Volume" entry is greyed out when the unallocated space is not adjacent to C:, or when an OEM recovery partition sits immediately to the right of C: — this is a Windows partition-layout constraint, not a data problem | — |
| Scope | Same-disk, in-place space reallocation. Not a cloning tool and not a whole-disk migration tool | Built into Windows | Broader partition-suite scope |

Common tools in the third-party category: AOMEI Partition Assistant, MiniTool Partition Wizard, EaseUS Partition Master, DiskGenius, Lazesoft, GParted Live USB.

**How to choose**

- Windows can already extend C: because the unallocated space sits right next to it: the built-in Disk Management is enough.
- The unallocated space exists but is not adjacent to C:, and you do not want to clone your whole disk: that is the situation ScsExpand addresses.
- You want to rebuild or clone the whole disk, or move it to a different machine: that is a full-disk migration / cloning product, not ScsExpand.

Full side-by-side walkthrough: **[ScsExpand vs MiniTool Partition Wizard and other partition tools](https://expand.scsoi.com/compare/minitool-partition-wizard-alternative)**.

## Download

Latest builds: **[GitHub Releases](https://github.com/shuyingegit/scsexpand/releases/latest)** · [Website](https://expand.scsoi.com/#download)

| Package | Use when |
|--------|----------|
| **Portable (`.zip`)** | Unzip and run — recommended (roughly 64 MB) |
| **Installer (`.exe`)** | Classic setup (roughly 64 MB) |

Requirements: Windows 10 / 11 (64-bit)

> **Note**
> This public repository hosts **release binaries only** (mirrored from the official CDN). Product source code is not published here.

## Free quota and licensing

The free download includes **1 expand, up to 5 GB**. The free version is a quota, not a time-limited trial — it is counted by expand count and size, not by trial days. After buyout the expand count and size are unlimited — limited only by the free space on the disk.

A license is bound to **one PC** and cannot be transferred to another device. Organisations that need one purchase to cover several PCs can arrange multi-device seats by email.

Pricing and current plans are listed on the official site: https://expand.scsoi.com/

## Official site and guides

- Home: https://expand.scsoi.com/
- FAQ: https://expand.scsoi.com/faq
- Comparison — ScsExpand vs MiniTool Partition Wizard and other partition tools: https://expand.scsoi.com/compare/minitool-partition-wizard-alternative
- Guide — how to expand the C: drive on the same disk: https://expand.scsoi.com/guide/expand-c-drive-same-disk

## Sister products

- **[ScsDrive](https://github.com/shuyingegit/scsdriver)** — [drive.scsoi.com](https://drive.scsoi.com) — mount WebDAV / NAS / cloud storage as a real Windows local disk.
- **[ScsSubst](https://github.com/shuyingegit/scssubst)** — [subst.scsoi.com](https://subst.scsoi.com) — map an existing local folder to a drive letter — shorter paths, no file copying.

More from SCSOI — [SCSOI company site](https://scsoi.com)

## FAQ

**Why is "Extend Volume" greyed out in Disk Management?**  
Mostly because the unallocated space is not adjacent to C:. Shrinking D: leaves the unallocated space at the end of the disk, and Windows can only extend a volume into unallocated space that sits immediately to its right. Another common cause is an OEM recovery partition sitting between C: and the free space. This is a Windows partition-layout constraint, not a data problem.

**Can I expand C: without reformatting or reinstalling Windows?**  
Yes. ScsExpand grows C: using free space from another partition on the same physical disk, and it neither reformats nor reinstalls anything. Your files stay where they are; only the space allocation changes.

**Does ScsExpand move or copy my files?**  
No. ScsExpand only changes how the free space on the same physical disk is allocated between partitions. Files on both the C: drive and the partition you take the space from stay in place. Back up important data before you expand anyway.

**Do I need a second disk or a USB drive?**  
No. ScsExpand works entirely inside the same physical disk, so no second disk, no external drive and no full-disk copy are involved. That is also why it is not a cloning tool.

**Is ScsExpand a cloning or whole-disk migration tool?**  
No. ScsExpand is not a full-disk migration, cloning or "move to a new PC" tool — that is a different product category. ScsExpand reallocates free space within one physical disk.

**Will programs I already have open block the expansion?**  
No. The heavy work runs in a guided restart environment, so programs you already have open do not block the volume while it is resized.

**How much can I expand for free?**  
The free download includes 1 expand, up to 5 GB. After buyout the expand count and size are unlimited, limited only by the free space on the disk.

**Can I move my license to another PC?**  
No. A license is bound to one PC and cannot be transferred to another device. Business users who need one purchase for several PCs can email support@scsoi.com to arrange multi-PC seats.

**Which Windows versions does ScsExpand support?**  
Windows 10 and Windows 11 (64-bit). There is no 32-bit, macOS or Linux build.

**Does ScsExpand mount cloud drives or give folders drive letters?**  
No. Mounting WebDAV, NAS or cloud storage as a real local disk is ScsDrive (https://drive.scsoi.com/), and mapping an existing local folder to a drive letter is ScsSubst (https://subst.scsoi.com/). ScsExpand is only about partition space on one physical disk.

**Where do I download ScsExpand?**  
From the official site (https://expand.scsoi.com/#download) or from the GitHub releases page. A portable zip (roughly 64 MB, recommended) and a setup installer (roughly 64 MB) are published for both.

## License & terms

Terms · Privacy · Refunds — [https://expand.scsoi.com/terms](https://expand.scsoi.com/terms) · [https://expand.scsoi.com/privacy](https://expand.scsoi.com/privacy) · [https://expand.scsoi.com/refund](https://expand.scsoi.com/refund)

## Support and disclosure

ScsExpand is developed and published by SCSOI — we are the vendor of this product, not a neutral third-party reviewer. Questions, bug reports and purchase questions all reach the same inbox: **support@scsoi.com**. Every plan, including the free version, includes email support and ongoing feature updates.

---

<p align="center">
  <a href="https://expand.scsoi.com/"><strong>Open website →</strong></a>
</p>

<p align="center">
  ScsExpand · <a href="https://drive.scsoi.com/">ScsDrive</a> · <a href="https://subst.scsoi.com/">ScsSubst</a> · <a href="https://scsoi.com/">SCSOI company site</a> · support@scsoi.com
</p>
