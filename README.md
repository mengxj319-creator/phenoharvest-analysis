# phenoharvest-analysis

气孔空间分布分析工具 - Ripley's K、Moran's I、KDE 等空间统计工具。纯网页版本，下载后即可直接使用。

気孔の空間分布解析ツール - Ripley's K、Moran's I、KDE などの空間統計ツール。軽量なWeb版で、ダウンロード後すぐに利用できます。

Stomatal spatial distribution analysis toolkit featuring Ripley's K, Moran's I, and KDE-based spatial statistics. A lightweight web-based version that works immediately after download.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen)](https://mengxj319-creator.github.io/phenoharvest-analysis/)

---

## Repository Description

Browser-based toolkit for stomatal annotation and spatial distribution analysis, including Ripley's K, Moran's I, single-image KDE, and multi-image mean/std KDE.

License check:

- README badge: `MIT`
- `LICENSE` file: standard MIT License
- Status: consistent

Suggested GitHub short description:

`Browser-based stomatal spatial analysis toolkit with Ripley's K, Moran's I, and KDE tools.`

---

## Overview

This repository provides a set of standalone browser tools for stomatal spatial analysis. No installation, backend, or Python environment is required. Each tool is distributed as a pure HTML page and can be opened directly in a browser.

Current modules include:

| Tool | Purpose | Analysis Method |
|:---|:---|:---|
| **Ripley's K** | Spatial point pattern analysis | Detect clustered / regular / random patterns |
| **Moran's I** | Spatial autocorrelation analysis | Polygon annotation + spatial weights matrix |
| **Single-image KDE** | Kernel density estimation | Heatmap visualization for one image |
| **Multi-image Mean/Std KDE** | Batch density analysis | Cross-image mean density and variation |

---

## Quick Start

1. Download this repository or the required HTML file.
2. Open the target file in your browser.
3. Upload microscopy images (`JPG`, `PNG`, `TIFF`, `BMP` supported in relevant tools).
4. Annotate stomata locations:
   - **Ripley's K / KDE**: draw rectangular boxes
   - **Moran's I**: draw polygons by clicking
5. Adjust parameters and generate results with one click.

**All computations are performed locally in the browser. No image or annotation data is uploaded to a server.**

---

## File List

### Single-image KDE

- `Phenoharvest_single_KDE_cn.html`
- `Phenoharvest_single_KDE_en.html`
- `Phenoharvest_single_KDE_ja.html`

### Multi-image Mean / Std KDE

- `Phenoharvest_multi_Mean_KDE_and_std_KDE_cn.html`
- `Phenoharvest_multi_Mean_KDE_and_std_KDE_en.html`
- `Phenoharvest_multi_Mean_KDE_and_std_KDE_ja.html`

### Multi-image Moran's I

- `Phenoharvest_multi_Moran's_I_cn.html`
- `Phenoharvest_multi_Moran's_I_en.html`
- `Phenoharvest_multi_Moran's_I_ja.html`

### Ripley's K

- `Phenoharvest_ripley's_K_cn.html`
- `Phenoharvest_ripley's_K_en.html`
- `Phenoharvest_ripley's_K_ja.html`

---

## Keyboard Shortcuts

| Key | Function |
|:---|:---|
| `D` | Draw mode |
| `S` | Select / move mode |
| `Ctrl + Z` | Undo |
| `Delete` / `Backspace` | Delete selected annotation |
| `ESC` | Cancel current operation |

Note:

- Shortcut behavior may differ slightly between tools.
- Moran's I uses polygon annotation, while KDE / Ripley's K mainly use box annotation.

---

## Import / Export

### Supported Import

- **Images**: `.jpg` `.png` `.tiff` `.bmp`
- **Annotations**: COCO JSON format

### Supported Export

| Format | Contents |
|:---|:---|
| CSV | Coordinates, area, Moran's I statistics, Ripley's K data, KDE statistics |
| PNG | Heatmaps, Ripley's K / L plots |
| COCO JSON | Annotation data for reuse or model training |

---

## Scientific Methods

| Tool | Core Algorithm | Output |
|:---|:---|:---|
| Ripley's K | K(d) -> L(d) transform | Clustered / regular / random pattern judgment + confidence interval |
| Moran's I | Spatial weights matrix + permutation test | I value, Z-score, P-value, HH / HL / LH / LL quadrants |
| KDE | Gaussian kernel density estimation | Density heatmap + contour levels |
| Mean/Std KDE | Cross-image density aggregation | Mean density field + standard deviation field |

---

## Technology Stack

1. Core: Vanilla JavaScript + HTML5 Canvas API
2. Styling: Tailwind CSS (CDN)
3. Icons: Heroicons
4. Fonts: Inter + JetBrains Mono

---

## Local Usage

```bash
# Clone the repository
git clone https://github.com/mengxj319-creator/phenoharvest-analysis.git

# Enter the folder
cd phenoharvest-analysis

# Open any HTML file directly in your browser
open Phenoharvest_ripley's_K_en.html      # macOS
start Phenoharvest_ripley's_K_en.html     # Windows
```

You can also simply double-click the HTML files in your file explorer.

---

## Citation

If you use this tool, please cite it via the CITATION.cff file.

---

## Contribution

Issues and Pull Requests are welcome.

You can contribute by:

1. Reporting bugs
2. Suggesting new features
3. Improving documentation
4. Expanding multilingual support

Chinese, Japanese, and English issue reports are all welcome.

---

## Language Notes

- `cn` = Chinese
- `en` = English
- `ja` = Japanese

The English pages are available in this version.
