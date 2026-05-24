# VisionCreator — Project Page

This folder contains the official project webpage for:

> **VisionCreator: A Native Visual-Generation Agentic Model with Understanding, Thinking, Planning and Creation**
> Jinxiang Lai, Zexin Lu, Jiajun He, Rongwei Quan, Wenzhe Zhao, Qinyu Yang, Qi Chen, Qin Lin,
> Chuyue Li, Tao Gao, Yuhao Shan, Shuai Shao, Song Guo, Qinglin Lu.
> Tencent Hunyuan × HKUST.

The page style follows the [CRPO project page](https://ddz16.github.io/crpo.github.io/) with a
clean academic layout.

---

## 📁 Directory layout

```
project_html/
├── index.html                # Main page
├── README.md                 # This file
└── static/
    ├── css/style.css         # Stylesheet
    ├── js/main.js            # Tab switching & BibTeX copy
    ├── images/               # Figures used by the page
    │   ├── fig1.png              # Framework comparison (teaser)
    │   ├── framework.png         # Overall PST + VRL framework
    │   ├── radar.png             # Radar plot, main result
    │   ├── visionagent.png       # Metacognition-based VisionAgent
    │   ├── data_gen.png          # Data generation pipeline
    │   ├── visgendata.png        # VisGenData-4k stats
    │   ├── visgenbench.png       # VisGenBench overview
    │   ├── virtual_env.png       # VisGenEnv (36 tools)
    │   ├── reward.png            # LtrReward
    │   ├── theorem.png           # Sim-to-real theorem
    │   ├── human.png             # Human evaluation
    │   ├── vis_compare.png       # Qualitative comparison
    │   ├── vis_1.png … vis_7.png # Visualization gallery
    │   ├── demo1.png, demo2.png  # Demo trajectories
    │   └── hunyuan_hkust_logo.png
    └── pdfs/
        └── VisionCreator.pdf     # Paper
```

All images were generated from the LaTeX source under
`../arXiv/VisionCreator (arXiv)_0303_2/figs/` and
`../arXiv/figs_large/`.

---

## 🚀 Local preview

The page is fully static — open it directly with a browser, **or** start a tiny local server
(recommended, since some browsers block local image loading without a server):

```bash
# Python 3
cd project_html
python3 -m http.server 8000
# then open http://localhost:8000
```

```bash
# Or with Node.js
npx http-server project_html -p 8000
```

---

## 🌐 Deploy on GitHub Pages

1. Create a new public repository, e.g. `visioncreator.github.io` (or any name).
2. Copy the **contents** of `project_html/` into the repo root:

   ```bash
   cp -r project_html/* /path/to/your-repo/
   cd /path/to/your-repo
   git init
   git add .
   git commit -m "init: VisionCreator project page"
   git branch -M main
   git remote add origin git@github.com:<user>/<repo>.git
   git push -u origin main
   ```

3. In the repo settings → **Pages** → Source: `Deploy from a branch` → branch `main` / root.
4. Wait ~1 min, the site will be live at
   `https://<user>.github.io/<repo>/`.

> ⚠️ The PDF file (`static/pdfs/VisionCreator.pdf`) is ~17 MB. If you prefer
> not to push it to git, host it on arXiv / OSS / Tencent COS and update the
> link in `index.html` (search for `static/pdfs/VisionCreator.pdf`).

---

## ✏️ How to customize

| Element                | Where to edit (`index.html`)                            |
| ---------------------- | ------------------------------------------------------- |
| Title / authors        | `<header class="hero">` block                           |
| arXiv / Code / HF links| The `.button-row` block at the bottom of the hero       |
| Abstract               | `Abstract` section (`.abstract-box`)                    |
| Stats (UTPC / 4k / 36) | `.stats` block under abstract                           |
| Contributions          | `.cards-grid` in the *Native Agentic Paradigm* section  |
| Method steps           | `.method-list` ordered list                             |
| Visualization gallery  | `.tabs` + `.tab-panel` blocks                           |
| BibTeX                 | `<pre id="bibtex-code">` block                          |

Replace placeholder URLs (`https://arxiv.org/`, `https://github.com/`,
`https://huggingface.co/`) with the real ones once they are published.

---

## 📷 Image source mapping

The mapping between the page images and the original LaTeX figures used in
`main.tex` (sections 0–9) is summarized below:

| Page image               | LaTeX figure                                    | Used in section |
| ------------------------ | ----------------------------------------------- | --------------- |
| `fig1.png`               | `\includegraphics{figs/fig1.png}` (Fig. 1)      | Introduction    |
| `radar.png`              | `figs/radar.png` (Fig. radar)                   | Introduction / Results |
| `framework.png`          | `figs/framework.png`                            | Method          |
| `visionagent.png`        | `figs/visionagent.png`                          | Data            |
| `data_gen.png`           | `figs/data_gen.png`                             | Data            |
| `visgendata.png`         | `figs/visgendata.pdf` (rasterized)              | Data            |
| `visgenbench.png`        | `figs_large/visgenbench.png`                    | Benchmark       |
| `virtual_env.png`        | `figs/virtual_env.png`                          | VisGenEnv       |
| `reward.png`             | `figs/reward.pdf`                               | VRL             |
| `theorem.png`            | `figs/theorem.pdf`                              | Theory          |
| `human.png`              | `figs_large/human.png`                          | Results         |
| `vis_compare.png`        | `figs/vis_compare.pdf`                          | Qualitative     |
| `vis_1.png … vis_7.png`  | `figs/vis_1.pdf … vis_7.pdf`                    | Gallery         |
| `demo1.png, demo2.png`   | `figs/demo1.pdf, demo2.pdf`                     | Gallery         |

---

## 🙏 Acknowledgement

The page layout follows the conventions of recent academic project pages,
in particular [Nerfies](https://nerfies.github.io/) and
[CRPO](https://ddz16.github.io/crpo.github.io/).
