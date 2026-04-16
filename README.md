<!-- badges: start -->
[![](img/license-badge.svg)](LICENSE.md)
[![](img/license-badge-ccby.svg)](data/LICENSE.md)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)
<!-- badges: end -->

<h1> Solar-Powered Glass Tumbler for Cape Maclear, Malawi: Design, Maintenance, Operation, and Results </h1>

**Contributors**

- **Emma Steinke** &mdash; [![ORCID](https://info.orcid.org/wp-content/uploads/2019/11/orcid_16x16.png) 0009-0005-9115-9379](https://orcid.org/0009-0005-9115-9379) &mdash; *design, construction, testing, writing*
- **Jakub Tkaczuk** &mdash; [![ORCID](https://info.orcid.org/wp-content/uploads/2019/11/orcid_16x16.png) 0000-0001-7997-9423](https://orcid.org/0000-0001-7997-9423) &mdash; *supervision, page development & maintenance*
- **Elizabeth Tilley** &mdash; [![ORCID](https://info.orcid.org/wp-content/uploads/2019/11/orcid_16x16.png) 0000-0002-2095-9724](https://orcid.org/0000-0002-2095-9724) &mdash; *supervision*

<br>
<p align="middle">
<img src="img/ETH_GHE_logo.svg" width=600>
<br><br>
<!-- This work is certified by the Open Source Hardware Association.<br \>
<a href="https://certification.oshwa.org/XXXXXXXX.html"><img src="img/certification-mark-XXXXXXXX-wide.svg" width=300></a>
<br> -->
<b>Complete description of system design, functionalities, operation, and maintenance is available on:<br \>
<a href="https://global-health-engineering.github.io/glass-tumbler/">Github pages</a>.
</b>
</p>

# Background

This repository details the construction, operation, and maintenance of the solar-powered glass tumbler built as part of a collaboration between the Malawian nonprofit organization, Sustainable Cape Maclear, and the Global Health Engineering Group at ETH Zürich.

Cape Maclear is a rural Malawian town located within a UNESCO World Heritage Site, which has attracted significant tourism and growth in the last 20 years. This has led to a unique waste challenge: an abundance of non-returnable glass bottles that are not part of a deposit system. The accumulation of broken glass creates sharp fragments that pose significant injury risks to residents, tourists, and wildlife.

Because industrial recycling is not economically or technically feasible in this location, the tumbler uses **glass tumbling** to grind away sharp edges, producing smooth "sea glass" that is safe for reuse in construction, landscaping, and jewelry. The machine is a standalone, solar-powered rotating drum system designed to process 20 kg batches of glass with a total material cost of approximately **$581.10**.

![](img/tumblerOverview.png)

# PDF Documentation

The full detailed guide and the quick start guide are available in the [`doc`](doc/) directory:

- [`doc/detailed_guide.pdf`](doc/detailed_guide.pdf)  
- [`doc/quickstart_guide.pdf`](doc/quickstart_guide.pdf)

CAD models and technical drawings are available in the [`cad`](cad/) directory.

# License

Different parts of this repository are released under different licenses, following standard practice for open-hardware research projects:

| Component | License |
| :--- | :--- |
| Hardware design (CAD, drawings, STEP files in [`cad/`](cad/)) | [CERN-OHL-S v2](LICENSE.md) |
| Documentation (qmd pages, guides in [`doc/`](doc/), this README) | [CC-BY-4.0](doc/LICENSE.md) |
| Datasets ([`data/`](data/)) | [CC-BY-4.0](data/LICENSE.md) |
