---
binder_popup: "[binder-link]{:target='_blank'}"
binder_button: "[![Launch Binder](https://mybinder.org/badge_logo.svg)][binder-link]{:target='_blank'}"
github_button: "[![View on Github](../badges/github.svg)][repo-link]"
zipball_button: "[![Download Zip](../badges/zip.svg)][zipball-link]"
tarball_button: "[![Download TarGz](../badges/tgz.svg)][tarball-link]"
---

{{ page.binder_button }}&nbsp;
{{ page.github_button }}&nbsp;
{{ page.zipball_button }}&nbsp;
{{ page.tarball_button }}&nbsp;
![last updated][last-updated-badge]

**A Tufts University Data Lab Workshop**\
Written by {{ site.author }}

[![datalab.tufts.edu](../badges/datalab.svg)](https://sites.tufts.edu/datalab)&nbsp;
[![@TuftsDataLab](../badges/twitter.svg)](https://twitter.com/intent/follow?screen_name=tuftsdatalab)

Slides: [tufts.box.com/v/{{ site.slides }}](https://tufts.box.com/v/{{ site.slides }})\
Live offerings: [go.tufts.edu/workshops](https://go.tufts.edu/workshops)\
Contact: <datalab-support@elist.tufts.edu>

---
## Table of Contents {#toc}

- [Workshop Overview](#overview)
- [Running the Workshop Notebook using a Virtual JupyterLab Instance (Recommended)](#binder)
- [Running the Workshop Notebook using a Local Anaconda or Mambaforge Installation](#local)

---
## Workshop Overview {#overview}

<!-- DO NOT CHANGE ANYTHING ABOVE THIS LINE -->

This hands-on interactive workshop demonstrates implementing a raster risk analysis using open-source Python libraries. The workshop notebook is suitable for self-guided study and covers the following:

- **Reading** raster datasets and exploring raster **attributes**
- **Visualizing**, **reclassifying**, and **masking** raster datasets
- Working with **digital elevation models**
- Reading and **rasterizing** vector data
- Calculating **euclidean distance rasters**
- Performing **zonal statistics**


<!-- DO NOT CHANGE ANYTHING BELOW THIS LINE -->

The notebook is designed to be run in a pre-configured cloud-computing environment via [Binder](#binder) and does not require the installation of any software. It is also possible to run the workshop notebook using a [local Anaconda or Mambaforge installation](#local). Instructions on how to install Anaconda or Mambaforge are available here: [go.tufts.edu/installingPython](https://go.tufts.edu/installingPython)

---
## Running the Workshop Notebook using a Virtual JupyterLab Instance (Recommended) {#binder}

{{ page.binder_button }}

1. Click on the [**Launch Binder**]{{ page.binder_popup }} button above.
2. A Binder instance will launch in a new tab with the message *Starting Repository*.
3. Wait patiently and do not close the Binder tab. After a few minutes, a **JupyterLab** instance will launch.
4. If the workshop notebook does not automatically open, *double-click* on `{{ site.file }}` in the file browser on the left.

---
## Running the Workshop Notebook using a Local Anaconda or Mambaforge Installation {#local}

{{ page.zipball_button }}&nbsp;
{{ page.tarball_button }}

1. Launch a **Conda-Enabled** Terminal or Command Prompt.
    - **Windows (Anaconda)**: *Start > Anaconda3 > Anaconda Prompt*
    - **Windows (Mambaforge)**: *Start > Mambaforge > Mambaforge Prompt*
    - **macOS**: *Applications > Utilities > Terminal*
2. Run the following commands by typing or pasting the command into the console and then pressing <kbd>Enter</kbd> or <kbd>Return</kbd>.
    - Download and extract the workshop materials:\
      `curl -Lo - https://github.com/tuftsdatalab/{{ site.repo }}/archive/workshop.tar.gz | tar -xzf -`
    - Navigate into the extracted directory: `cd {{ site.repo }}-workshop`
    - Create a new environment for the workshop.
        - **Anaconda**: `conda env create -f environment.yml`
        - **Mambaforge**: `mamba env create -f environment.yml`
    - Activate the workshop environment: `conda activate {{ site.env }}`
    - Open the workshop notebook in JupyterLab: `jupyter lab {{ site.file }}`
3. JupyterLab will launch in a web browser. (A new tab will be generated if a browser is already open.)
4. If the workshop notebook does not automatically open, *double-click* on `{{ site.file }}` in the file browser on the left.
5. **Do not close the console!** Closing the console will also terminate JupyterLab. Leave the console running in the background.


[binder-link]: https://mybinder.org/v2/gh/tuftsdatalab/{{ site.repo }}/binder?urlpath=lab/tree/{{ site.file }}
[repo-link]: https://github.com/tuftsdatalab/{{ site.repo }}
[zipball-link]: https://github.com/tuftsdatalab/{{ site.repo }}/archive/workshop.zip
[tarball-link]: https://github.com/tuftsdatalab/{{ site.repo }}/archive/workshop.tar.gz
[last-updated-badge]: https://img.shields.io/github/last-commit/tuftsdatalab/{{ site.repo }}?label=last%20updated
