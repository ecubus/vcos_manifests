# manifests代码仓库说明

## 1. 代码仓库简介

Manifest（清单文件）是软件开发中用于管理多仓库项目的核心配置文件，主要用于定义代码库的组成结构和依赖关系。在大型项目（如 Android 开源项目 AOSP）中，通常需要协同管理数十甚至数百个独立的 Git 仓库，而 Manifest 文件（如 default.xml）则通过统一的规则声明这些仓库的地址、分支、版本以及同步方式，确保整个项目能保持一致性和可复现性

理想星环OS（HaloOS）是理想汽车自主研发的整车级开源操作系统，包括了像智能车控OS（VCOS）、通信中间件（VBS）、辅助驾驶OS（ADOS）等多个子系统。通过不同的xml文件可以选择下载理想开源项目中全部仓库或者指定子系统的仓库

## 2. 代码目录

manifests 源代码在 haloosspace/.repo/manifests 目录下，目录结构如下图所示

```bash
haloosspace
└── .repo
    └── manifests        # manifests 仓库
        ├── default.xml  # 理想开源项目中全部仓库
        ├── vbslite.xml  # 通信中间件（VBS）子系统的全部仓库
        ├── vcos.xml     # 智能车控OS（VCOS）子系统的全部仓库
        └── {other}.xml  # 其它子系统，待补充
```

## 3. 仓库使用入门

**Manifest文件列表：**

|文件名|功能|
|---|---|
|default.xml|理想开源项目中全部仓库|
|vbslite.xml|通信中间件（VBS）子系统的全部仓库|
|vcos.xml|智能车控OS（VCOS）子系统的全部仓库|
|{other}.xml|其它子系统，待补充|

**代码下载：**

```bash
## repo 固定下载代码格式 ##
repo init -u <manifest URL> -b <branch name> -m <manifest.xml>
repo sync
```

```bash
## HaloOS项目全量仓库下载 ##
repo init -u git@gitee.com:haloos/manifests.git -b master -m default.xml
repo sync
```

```bash
## VBS子系统全量仓库下载 ##
repo init -u git@gitee.com:haloos/manifests.git -b master -m vbslite.xml
repo sync
```

```bash
## VCOS子系统全量仓库下载 ##
repo init -u git@gitee.com:haloos/manifests.git -b master -m vcos.xml
repo sync
```
