# Tutorials

During the Hackathon, we will be running hands-on tutorials to demonstrate how to use the open-source software needed to access and analyse Near-Present Day simulation outputs stored in the cloud.

For those with limited Python experience, we would recommend working through **Tutorial 0. Getting Started with xarray** prior to the hackathon to better understand the key data structures and operations used throughout the hackathon.

---

### **Pre-Hackathon**

* **0. Getting Started with xarray**

    Ocean models produce large, multi-dimensional fields (e.g. temperature, salinity, velocity) that vary in time and space and are described by physical coordinates (e.g., depth). [**xarray**](https://docs.xarray.dev/en/stable/) provides data structures that explicitly represent these dimensions and coordinates, rather than treating model outputs as anonymous multi-dimensional arrays.

    This Jupyter Notebook provides an introduction to xarray for ocean model analysis and is intended as a quick reference that you can return to during the hackathon and beyond.

---

### **Day 1**

* **1. Getting Started with OceanDataStore to access NOC NPD data via the cloud.**

    In this Jupyter Notebook, we will demonstrate how to use the **OceanDataCatalog** API to explore the [**Near-Present-Day**](https://noc-msm.github.io/NOC_Near_Present_Day/) global ocean sea-ice simulations developed by the National Oceanography Centre as part of the Atlantic Climate and Environment Strategic Science ([**AtlantiS**](https://noc.ac.uk/projects/atlantis)) programme.

    We will cover:

    * How to use the **OceanDataCatalog** to explore Spatio-Temporal Access Catalogs ([**STAC**](https://stacspec.org/en)) exposing available collections of ocean model & observational data stored in the JASMIN Object Store.

    * How to search the **OceanDataCatalog** by collection, variable name, standard name or platform.

    * How to open and subset Analysis-Ready Cloud-Optimised ([**ARCO**](https://doi.org/10.1109/MCSE.2021.3059437)) datasets as lazy [**xarray**](https://docs.xarray.dev/en/stable/user-guide/data-structures.html) Datasets.

* **2. Getting Started with NEMO Cookbook to analyse NOC NPD data.**

    In this Jupyter Notebook, we will demonstrate how to use the `NEMODataTree` object to analyse outputs of the [**Near-Present-Day**](https://noc-msm.github.io/NOC_Near_Present_Day/) global ocean sea-ice simulations.

    We will cover:

    * How to create `NEMODataTree` objects directly from netCDF files and Near-Present-Day outputs stored in the JASMIN object store using the **OceanDataCatalog**.

    * How to navigate and access NEMO output variables stored in a `NEMODataTree`.

    * How to open and subset Analysis-Ready Cloud-Optimised ([**ARCO**](https://doi.org/10.1109/MCSE.2021.3059437)) datasets as lazy [**xarray**](https://docs.xarray.dev/en/stable/user-guide/data-structures.html) Datasets.

---

### **Day 2**

* **3. Running your own experiments with NOC NPD.**

    In this tutorial, we will demonstrate how to quickly download and run custom experiments using the existing NOC Near-Present Day configurations. We will also hihglight some recent examples, including the development of a new nested configuration used to perform Observing System Simulation Experiments (OSSEs) for the RAPID-Evolution project.
