# <img src="https://user-images.githubusercontent.com/7437523/128596331-dc5c5e40-93e1-4d9e-b92d-9c53fe51145a.png" width="500"/>

[![License](https://img.shields.io/github/license/Jeevanjyotirout/seispy)]()
[![](https://img.shields.io/github/last-commit/Jeevanjyotirout/seispy)]()
[![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/Jeevanjyotirout/seispy)]()
[![GitHub repo size](https://img.shields.io/github/repo-size/Jeevanjyotirout/seispy)]()
[![Static Badge](https://img.shields.io/badge/DOI-10.1785%2F0220220288-pink)](https://doi.org/10.1785/0220220288)

[![Anaconda-Server Badge](https://anaconda.org/conda-forge/seispy/badges/version.svg)](https://anaconda.org/conda-forge/seispy)
[![Conda Version](https://img.shields.io/conda/vn/conda-forge/seispy.svg)](https://anaconda.org/conda-forge/seispy)
[![Anaconda-Server Badge](https://anaconda.org/conda-forge/seispy/badges/downloads.svg)](https://anaconda.org/conda-forge/seispy)

[![PyPI](https://img.shields.io/pypi/v/python-seispy)](https://pypi.org/project/python-seispy/)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/python-seispy)](https://pypi.org/project/python-seispy/)

[![GitHub stars](https://img.shields.io/github/stars/Jeevanjyotirout/seispy)]()

---

## About SeisPy

**SeisPy** is an advanced, professional-grade Python toolkit for seismological analysis and receiver function processing. Developed to address the growing computational demands in modern seismology, SeisPy provides researchers and geophysicists with a comprehensive suite of tools for analyzing seismic data, calculating receiver functions, and performing advanced subsurface imaging.

This project represents a commitment to delivering high-performance, scientifically rigorous solutions for the seismology community. With optimized algorithms, intuitive interfaces, and extensive functionality, SeisPy bridges the gap between theoretical geophysics and practical data analysis.

### Vision & Development Philosophy

SeisPy is built on the principle that modern seismological research requires tools that are both powerful and accessible. My vision for this project includes:

- **Robustness**: Ensuring reliable performance across diverse datasets and computing environments
- **Innovation**: Continuously integrating cutting-edge methodologies from published research
- **Usability**: Maintaining clean, well-documented code with intuitive command-line interfaces
- **Performance**: Leveraging NumPy and modern Python practices for computational efficiency
- **Integration**: Building seamlessly on top of ObsPy while extending its capabilities

### Key Features & Capabilities

- **Receiver Function Processing**: Complete workflow from raw seismic data to publication-ready results
- **Multiple Deconvolution Methods**: Time-domain iterative and frequency-domain water-level techniques
- **Advanced Imaging**: 2D/3D Common Conversion Point (CCP) stacking with moveout corrections
- **Crustal Analysis**: H-κ stacking, anisotropy estimation, and depth conversion
- **Quality Control**: Interactive visualization and manual picking tools
- **Modern Stack**: Built on ObsPy, NumPy, and Matplotlib for reliability and extensibility

### Future Development Roadmap

Ongoing enhancements and planned features include:

- Enhanced parallelization for large-scale batch processing
- Machine learning integration for automatic phase picking and quality assessment
- Extended support for additional seismic phases and wave types
- Improved visualization capabilities with interactive 3D rendering
- Comprehensive testing suite expansion

---

## Scientific Citations

When using SeisPy in your research, please cite the following publications as appropriate:

### Primary Reference

For general use of the SeisPy package, please cite:

* Xu, M. & He, J. (2023). Seispy: Python Module for Batch Calculation and Postprocessing of Receiver Functions. *Seismological Research Letters*, 94 (2A): 935–943. [![DOI](https://img.shields.io/badge/DOI-10.1785%2F0220220288-pink)](https://doi.org/10.1785/0220220288)

### Method-Specific Citations

#### 3D Time-Difference Correction

If using 3D time-difference correction methods, please also cite:

* Xu, M., Huang, H., Huang, Z., Wang, P., Wang, L., Xu, M., ... & Yuan, X. (2018). Insight into the subducted Indian slab and origin of the Tengchong volcano in SE Tibet from receiver function analysis. *Earth and Planetary Science Letters*, 482, 567-579. [![DOI](https://img.shields.io/badge/DOI-10.1016%2Fj.epsl.2017.11.048-blue)](https://doi.org/10.1016/j.epsl.2017.11.048)

* Xu, M., Huang, Z., Wang, L., Xu, M., Mi, N., & Yu, D. (2020). Lateral variation of the mantle transition zone beneath the Tibetan plateau: Insight into thermal processes during Indian–Asian collision. *Physics of the Earth and Planetary Interiors*, 301, 106452. [![DOI](https://img.shields.io/badge/DOI-10.1016%2Fj.pepi.2020.106452-blue)](https://doi.org/10.1016/j.pepi.2020.106452)

#### 2D and 3D CCP Stacking

For CCP stacking implementations, please also cite:

* Xu, M., Huang, Z., Wang, L., Xu, M., Zhang, Y., Mi, N., ... & Yuan, X. (2020). Sharp lateral Moho variations across the SE Tibetan margin and their implications for plateau growth. *Journal of Geophysical Research: Solid Earth*, 125(5), e2019JB018117. [![DOI](https://img.shields.io/badge/DOI-10.1029%2F2019JB018117-blue)](https://doi.org/10.1029/2019JB018117)

---

## Installation

SeisPy supports multiple installation methods to accommodate different workflows and environments.

### Quick Install (Recommended)

#### Via Conda (Recommended)

```bash
conda install -c conda-forge seispy
```

#### Via PyPI

```bash
pip install python-seispy
```

### Detailed Installation Instructions

For comprehensive installation guidance, including environment setup, dependency management, and troubleshooting, please refer to the [official documentation](https://seispy.xumijian.me/installation.html).

### System Requirements

- Python 3.7 or higher
- NumPy, SciPy, Matplotlib
- ObsPy 1.2.0 or higher
- Additional dependencies listed in project documentation

---

## Core Libraries

SeisPy is organized into modular libraries, each addressing specific aspects of seismological analysis:

### Distance & Azimuth Calculations

* **`seispy.distaz`**: High-performance distance and azimuth calculations with full `numpy.ndarray` support. Algorithm credited to the [USC Lithospheric Seismology Program](http://www.seis.sc.edu/software/distaz/), optimized for modern Python workflows.

### Geophysical Utilities

* **`seispy.geo`**: Collection of essential geophysical computation tools and utilities.

### Deconvolution Methods

* **`seispy.decon`**: Professional implementation of receiver function deconvolution techniques, adapted from [iwbailey/processRFmatlab](https://github.com/iwbailey/processRFmatlab):
  * Iterative time-domain deconvolution (Ligorría & Ammon, 1999)
  * Water-level frequency-domain deconvolution (Ammon, 1991)

### Receiver Function Workflow

* **`seispy.rf`**: Complete receiver function calculation pipeline with earthquake catalog management, station matching, and batch processing. Leverages `obspy.core.UTCDateTime` and `obspy.clients` for seamless FDSN integration.

### Event Processing

* **`seispy.eq`**: Event-specific RF processing module with comprehensive SAC format support, signal processing capabilities, and TauP toolkit integration via [ObsPy](https://docs.obspy.org/).

### Crustal Structure Analysis

* **`seispy.hk`**: H-κ stacking implementation for Moho depth and Vp/Vs ratio estimation (Zhu & Kanamori, 2000).

### Anisotropy Analysis

* **`seispy.rfani`**: Joint inversion method for crustal anisotropy characterization (Liu & Niu, 2011).

### Slant Stacking

* **`seispy.slantstack`**: Slant stack analysis for single stations (Tauzin et al., 2008).

### RF Correction & Conversion

* **`seispy.rfcorrect`**: Advanced post-processing including moveout correction and time-to-depth conversion (1D and 3D velocity models). Methodology detailed in [Xu et al., 2018](https://www.sciencedirect.com/science/article/pii/S0012821X17306921?via%3Dihub).

### CCP Stacking

* **`seispy.ccpprofile`**: 2D CCP stacking along user-defined profiles.
* **`seispy.ccp3d`**: Full 3D CCP stacking with automatic D410 and D660 discontinuity extraction.

---

## Command-Line Tools

SeisPy provides a comprehensive suite of command-line utilities for all stages of receiver function analysis:

### Receiver Function Processing

* **`prf`**: Calculate P-wave receiver functions for single or multiple stations
* **`pickrf`**: Interactive quality control and manual RF selection interface
* **`plotrt`**: Visualize R and T component RFs organized by back-azimuth
* **`plotr`**: Plot R component RFs with back-azimuth sorting
* **`hk`**: Perform H-κ stacking to estimate Moho depth and Vp/Vs ratio
* **`rf2depth`**: Convert time-domain RFs to depth-domain representations
* **`ccp_profile`**: Generate CCP stacked cross-sections along profiles
* **`ccp3d`**: Perform 3D CCP stacking in gridded volumes
* **`rfani`**: Estimate crustal anisotropy using joint inversion methods
* **`rfharmo`**: Harmonic decomposition analysis for dip and anisotropic components
* **`pickdepth`**: Interactive depth picking tool for stacked RF volumes

### Utility Commands

* **`veltxt2mod`**: Convert ASCII velocity tables to optimized NumPy `.npz` 3D model format
* **`download_catalog`**: Fetch earthquake catalogs directly from FDSN web services
* **`gen_rayp_lib`**: Generate ray parameter lookup libraries for given source depths and distances
* **`setpar`**: Command-line configuration file editor for SeisPy parameters

---

## Documentation & Support

Comprehensive documentation, tutorials, and examples are available at:

**[https://seispy.xumijian.me/](https://seispy.xumijian.me/)**

---

## Contributing

Contributions, bug reports, and feature requests are welcome. Please feel free to open issues or submit pull requests to help improve SeisPy.

---

## License

SeisPy is released under the [GNU General Public License v3.0](LICENSE.txt).

---

## Acknowledgments

This project builds upon and extends methodologies from the broader seismology community. Special recognition to:

- The ObsPy development team for their foundational seismology framework
- Contributors to the original algorithms and methods cited in scientific publications
- The seismology research community for continued feedback and collaboration

---

*Maintained by Jeevan Jyoti Rout | For questions or collaborations, please open an issue on GitHub.*
