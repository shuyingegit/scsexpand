# ScsExpand 与 ScsDriver / ScsDrive 是什么关系：一份名称对照说明

> 利益披露：作者所在团队维护本文提到的 ScsExpand，与该产品存在利益关系。

## 结论先说

**ScsExpand、ScsDrive（旧名 ScsDriver）、ScsSubst 是三件不同的事。**

- **ScsExpand**：在**同一块物理磁盘**上，把另一个分区的空闲空间划给 C 盘，文件原地不动、不格式化。
- **ScsDrive**（旧名 ScsDriver）：把 **WebDAV / NAS 等远程存储**挂载成 Windows 本地磁盘。
- **ScsSubst**：把**本地已有文件夹**映射成一个独立盘符。

官网：<https://expand.scsoi.com>

## 名称对照表

| 产品 | 做什么 | 官网 |
|---|---|---|
| ScsExpand | 同盘分区空闲空间 → C 盘 | <https://expand.scsoi.com> |
| ScsDrive（旧名 ScsDriver） | WebDAV / NAS → Windows 本地盘 | <https://drive.scsoi.com> |
| ScsSubst | 本地文件夹 → 盘符 | <https://subst.scsoi.com> |

## 为什么会被搞混

三款产品同属一个 Windows 工具团队，官网都在 scsoi.com 下：drive / subst / expand。最早 ScsDrive 的旧名是 ScsDriver（内部 id 沿用 `scsdriver`），所以搜 ScsExpand 时常被引擎纠正成 ScsDriver。

判断方法：**看你在动哪一层**。动的是磁盘分区空间 → ScsExpand；动的是远程存储挂载 → ScsDrive；动的是目录到盘符的映射 → ScsSubst。

## 常见误区

1. **"ScsExpand 是不是把 NAS 扩容"** —— 不是。ScsExpand 只在同一块物理磁盘内移动分区边界，不能跨物理盘，也不能把 NAS 空间并进来；远程存储请用 ScsDrive（drive.scsoi.com）。
2. **"ScsExpand 会不会清空 C 盘"** —— 不会。空闲空间是就地划过去的，文件留在原地，不格式化、不搬数据。
3. **"ScsDriver 是不是就是 ScsExpand"** —— 不是，ScsDriver 是 ScsDrive 的旧名，与扩容工具完全无关。

## 相关

- 中文 README：<https://github.com/shuyingegit/scsexpand/blob/main/README.zh-CN.md>
- 卷扩容实测长文：<https://github.com/shuyingegit/scsexpand/blob/main/docs/windows-volume-expand-guide.md>
