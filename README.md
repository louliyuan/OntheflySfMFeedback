# On-the-fly Feedback SfM

**On-the-fly Feedback SfM:** An Explore-and-Exploit Framework for Real-Time UAV Photogrammetry.

[![arXiv](https://img.shields.io/badge/arXiv-2512.02375-b31b1b.svg)](https://arxiv.org/abs/2512.02375)

### Key Features

* **Online coarse mesh generation** from incrementally expanding sparse point clouds.
* **Real-time mesh quality assessment** with key quality metrics (GSD, observation redundancy, and reprojection error).
* **Predictive path planning & trajectory refinement** for optimized navigation guidance.


---

# Install Instructions

## Environment Setup

* Visual Studio 2022 (v17.9.1 recommended)
* Qt 5.12.12 (Core, Gui, OpenGL, Widgets)
* CUDA 12.2
* VCPKG

  * Run `vcpkg integrate install`
  * Install C++ dependencies via `vcpkg install`
* Intel® oneAPI Threading Building Blocks (TBB)
* Python environment

  * Install PyTorch:

    ```bash
    pip install torch==2.2.2 torchvision==0.17.2 torchaudio==2.2.2 --index-url https://download.pytorch.org/whl/cu118
    ```
  * Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```
  * Install `deep-image-matching`

## Build Instructions

### Build Order

Please strictly follow the order below to ensure correct dependency linking:

#### Third-party Libraries (`thirdparty`)

* SIFTGPU
* VLFeat

#### Internal Modules

* Base
* Geometry
* Scene
* Estimator
* Feature
* Workflow
* UI

## Citation

If you find this work useful in your research, please consider citing:

```bibtex
@misc{lou2025ontheflyfeedbacksfm,
  title={On-the-fly Feedback SfM: Online Explore-and-Exploit UAV Photogrammetry with Incremental Mesh Quality-Aware Indicator and Predictive Path Planning},
  author={Liyuan Lou and Wanyun Li and Wentian Gan and Yifei Yu and Tengfei Wang and Xin Wang and Zongqian Zhan},
  year={2025},
  eprint={2512.02375},
  archivePrefix={arXiv},
  primaryClass={cs.CV},
  doi={10.48550/arXiv.2512.02375},
  url={https://arxiv.org/abs/2512.02375}
}

