# phenoharvest-analysis
气孔空间分布分析工具 - Ripley's K, Moran's I, KDE 空间统计工具。纯网页版本下载就能用。

気孔の空間分布解析ツール ― RipleyのK関数、MoranのI、KDEなどの空間統計ツール。 簡単なWeb版で、ダウンロードするだけで使用可能です。

Stomatal Spatial Distribution Analysis Tool – Spatial statistics tools including Ripley’s K, Moran’s I, and KDE.
A pure web-based version that can be used immediately after download. English version on the way!!!

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen)](https://github.com/mengxj319-creator)

---

## 📊 功能模块

| 工具 | 用途 | 分析方法 |
|:---|:---|:---|
| **Ripley's K** | 空间点模式分析 | 检测聚集/规则/随机分布 |
| **Moran's I** | 空间自相关分析 | 多边形标注 + 空间权重矩阵 |
| **单图 KDE** | 核密度估计 | 单图像热力图可视化 |
| **多图 Mean/Std KDE** | 批量密度分析 | 跨图像密度平均与变异 |

---

## 🚀 快速开始

1. 下载对应文件，双击打开
2. 上传显微图像（支持 JPG/PNG/TIFF）
3. 标注气孔位置：
   - **Ripley's K / KDE**: 拖拽画框
   - **Moran's I**: 点击绘制多边形
4. 调整分析参数，一键生成结果

**⚡ 所有计算在浏览器本地完成，数据不会上传到服务器**

---

## ⌨️ 快捷键

| 按键 | 功能 |
|:---|:---|
| `D` | 画框/绘制模式 |
| `S` | 选择/移动模式 |
| `Ctrl + Z` | 撤销 |
| `Delete` / `Backspace` | 删除选中标注 |
| `ESC` | 取消当前操作 |

---

## 📁 数据导入导出

### 支持导入
- **图像**: `.jpg` `.png` `.tiff` `.bmp`
- **标注**: COCO JSON 格式（跨工具复用）

### 支持导出
| 格式 | 用途 |
|:---|:---|
| CSV | 坐标、面积、Moran's I 统计、Ripley's K 数据 |
| PNG | 热力图、L函数分析图 |
| COCO JSON | 标注数据（可用于训练检测模型）|

---

## 🔬 科学方法

| 工具 | 核心算法 | 输出指标 |
|:---|:---|:---|
| Ripley's K | K(d) → L(d) 变换 | 聚集/规则/随机判定 + 置信区间 |
| Moran's I | 空间权重矩阵 + 置换检验 | I指数、Z-score、P-value、HH/HL/LH/LL四象限 |
| KDE | 高斯核密度估计 | 密度热力图 + 等高线（0.3/0.5/0.7/0.9）|
| Mean/Std KDE | 跨图像密度聚合 | 平均密度场 + 标准差变异场 |

---

## 🛠️ 技术栈
1. 核心: Vanilla JavaScript + HTML5 Canvas API
2. 样式: Tailwind CSS (CDN)
3. 图标: Heroicons
4. 字体: Inter + JetBrains Mono
5. AI小帮手：Kimi 2.5 （非常好用 kimi code 吊打 codex）

---

## 📚 引用
@software{phenoharvest2026,
  author = {mengxj319-creator},
  title = {PhenoHarvest: Browser-based toolkit for stomatal spatial pattern analysis},
  url = {https://github.com/mengxj319-creator/phenoharvest-analysis},
  year = {2026}
}
---

## 🤝 贡献


欢迎提交 Issue 或 Pull Request：
1. 🐛 报告 Bug (中日英三种语言，用这三种比较好对应)
2. 💡 建议新功能
3. 📝 改进文档
4. 🌍 多语言支持


---

## 📊 機能モジュール

| ツール | 用途 | 分析手法 |
|:---|:---|:---|
| **Ripley's K** | 空間点パターン解析 | 集合・規則・ランダム分布の判定 |
| **Moran's I** | 空間自己相関解析 | ポリゴン注釈 + 空間重み行列 |
| **単一画像 KDE** | カーネル密度推定 | 単一画像のヒートマップ可視化 |
| **複数画像 Mean/Std KDE** | バッチ密度解析 | 画像間の平均密度と変動 |

---

## 🚀 クイックスタート

1. 対応ファイルをダウンロードし、ダブルクリックで起動  
2. 顕微鏡画像をアップロード（JPG/PNG/TIFF対応）  
3. 気孔位置をアノテーション：
   - **Ripley's K / KDE**: ドラッグで矩形描画  
   - **Moran's I**: クリックでポリゴン描画  
4. パラメータを調整し、ワンクリックで解析結果を生成  

**⚡ すべての計算はブラウザ上でローカル実行され、データはサーバーに送信されません**

---

## ⌨️ ショートカットキー

| キー | 機能 |
|:---|:---|
| `D` | 描画モード |
| `S` | 選択／移動モード |
| `Ctrl + Z` | 元に戻す |
| `Delete` / `Backspace` | 選択した注釈を削除 |
| `ESC` | 操作キャンセル |

---

## 📁 データ入出力

### インポート対応
- **画像**: `.jpg` `.png` `.tiff` `.bmp`
- **アノテーション**: COCO JSON形式（ツール間で再利用可能）

### エクスポート対応
| 形式 | 内容 |
|:---|:---|
| CSV | 座標・面積・Moran's I統計・Ripley's Kデータ |
| PNG | ヒートマップ・L関数解析図 |
| COCO JSON | アノテーションデータ（検出モデルの学習に利用可能）|

---

## 🔬 科学手法

| ツール | コアアルゴリズム | 出力指標 |
|:---|:---|:---|
| Ripley's K | K(d) → L(d)変換 | 分布判定（集合・規則・ランダム）+ 信頼区間 |
| Moran's I | 空間重み行列 + 置換検定 | I値、Zスコア、P値、HH/HL/LH/LL四象限 |
| KDE | ガウス核密度推定 | 密度ヒートマップ + 等高線（0.3/0.5/0.7/0.9） |
| Mean/Std KDE | 画像間密度集約 | 平均密度場 + 標準偏差変動 |

---

## 🛠️ 技術スタック

1. コア: Vanilla JavaScript + HTML5 Canvas API  
2. スタイル: Tailwind CSS（CDN）  
3. アイコン: Heroicons  
4. フォント: Inter + JetBrains Mono  
5. AI補助: Kimi 2.5（非常に使いやすく、Kimi CodeはCodexを凌駕）  

---

## 📚 引用

@software{phenoharvest2026,  
  author = {mengxj319-creator},  
  title = {PhenoHarvest: Browser-based toolkit for stomatal spatial pattern analysis},  
  url = {https://github.com/mengxj319-creator/phenoharvest-analysis},  
  year = {2026}  
}

---

## 🤝 コントリビューション

IssueやPull Requestは大歓迎です：

1. 🐛 バグ報告（中国語・日本語・英語のいずれかでご記入ください）
2. 💡 新機能の提案
3. 📝 ドキュメントの改善
4. 🌍 多言語対応の追加

## 💻 本地运行

---

```bash
# 克隆仓库
git clone https://github.com/mengxj319-creator/phenoharvest-analysis.git

# 进入目录
cd phenoharvest-analysis

# 用浏览器打开任意 HTML 文件即可使用
open Phenoharvest_repley's_K_cn.html      # macOS
start Phenoharvest_repley's_K_cn.html     # Windows






