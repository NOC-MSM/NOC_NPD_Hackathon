# Resources

Below we have provided a list of useful links to documentation and data sources to support group analyses during the hackathon event.

---

## **Documentation**

* **NOC Near-Present Day**

    [**https://noc-msm.github.io/NOC_Near_Present_Day/**](https://noc-msm.github.io/NOC_Near_Present_Day/)

* **OceanDataStore**

    [**https://noc-msm.github.io/OceanDataStore/**](https://noc-msm.github.io/OceanDataStore/)

* **NEMO Cookbook**

    [**https://noc-msm.github.io/nemo_cookbook/**](https://noc-msm.github.io/nemo_cookbook/)

* **ValidOcean**

    [**https://noc-msm.github.io/ValidOcean/**](https://noc-msm.github.io/ValidOcean/)

* **xarray Tutorial**

    [**https://tutorial.xarray.dev/intro.html**](https://tutorial.xarray.dev/intro.html)

* **Flox**

    [**https://flox.readthedocs.io/en/latest/**](https://flox.readthedocs.io/en/latest/)

* **Earth & Environmental Data Science Book**

    [**https://earth-env-data-science.github.io/intro.html**](https://earth-env-data-science.github.io/intro.html)

* **Cosima Cookbook**

    [**https://cosima-recipes.readthedocs.io/en/latest/**](https://cosima-recipes.readthedocs.io/en/latest/)

---

## **Data**

### **Ocean Observations**

The observational datasets below are accessible via the JASMIN object store using `xarray.open_zarr()` as follows:

```python
xr.open_zarr(url, zarr_format=3)
```

where the `url` is composed of a **Base URL** and **Available Dataset** (i.e., `url = <base_url>/<dataset>`)

---

**NSIDC Observations**
    
For further details, see NSIDC [**here**](https://nsidc.org/data/g02135/versions/4).

**Base URL:** 

```
https://noc-msm-o.s3-ext.jc.rl.ac.uk/ocean-obs/NSIDC/
```

**Available Datasets:**
 
* NSIDC_Sea_Ice_Index_v3_Antarctic/
* NSIDC_Sea_Ice_Index_v3_Arctic/
* NSIDC_Sea_Ice_Index_v4_Antarctic/
* NSIDC_Sea_Ice_Index_v4_Arctic/

---

**HadISST Observations**
    
For further details, see HadISST [**here**](https://www.metoffice.gov.uk/hadobs/hadisst/).

**Base URL:**

```
https://noc-msm-o.s3-ext.jc.rl.ac.uk/ocean-obs/HadISST/
```

**Available Datasets:**
 
* HadISST_global_monthly/

---

**OISSTv2 Observations**
    
For further details, see OISSTv2 [**here**](https://psl.noaa.gov/data/gridded/data.noaa.oisst.v2.highres.html).

**Base URL:** 

```
https://noc-msm-o.s3-ext.jc.rl.ac.uk/ocean-obs/OISSTv2/
```

**Available Datasets:**
 
* OISSTv2_siconc_global_climatology_1991_2020/
* OISSTv2_siconc_global_monthly/
* OISSTv2_sst_global_climatology_1991_2020/
* OISSTv2_sst_global_monthly/

---

**EN4.2.2 Analysis**
    
For further details, see EN4.2.2 [**here**](https://www.metoffice.gov.uk/hadobs/en4/download-en4-2-2.html).

**Base URL:**

```
https://noc-msm-o.s3-ext.jc.rl.ac.uk/ocean-obs/EN4/
```

**Available Datasets:**

* EN4.2.2_global_monthly/

---

**ARMOR-3D Analysis**
    
For further details, see ARMOR-3D [**here**](https://data.marine.copernicus.eu/product/MULTIOBS_GLO_PHY_TSUV_3D_MYNRT_015_012/description).

**Base URL:** 

```
https://noc-msm-o.s3-ext.jc.rl.ac.uk/ocean-obs/ARMOR3D/
```

**Available Datasets:**

* ARMOR3D_RP_global_monthly_1993_2022/

---

**RAPID Observations**
    
For further details, see RAPID Data [**here**](https://rapid.ac.uk/data).

**Base URL:**

```
https://noc-msm-o.s3-ext.jc.rl.ac.uk/ocean-obs/RAPID/
```

**Available Datasets:**

* 2d_gridded_v2024.1/
* fc_transport_adj_v3/
* meridional_transports_v2024.1/
* moc_transports_v2024.1/
* moc_vertical_v2024.1/
* mocha_mht_data_ERA5_v2020/
* ts_gridded_v2024.1/

---

**OSNAP Observations**
    
For further details, see OSNAP Data [**here**](https://www.o-snap.org/data-access/).

**Base URL:**

```
https://noc-msm-o.s3-ext.jc.rl.ac.uk/ocean-obs/OSNAP/
```

**Available Datasets:**

* OSNAP_Gridded_TSV_201408_202207_2025/
* OSNAP_MOC_MHT_MFT_TimeSeries_201408_202207_2025/
* OSNAP_Streamfunction_201408_202207_2025/

---

**World Ocean Atlas 2023 Analysis**

For further details, see World Ocean Atlas [**here**](https://www.ncei.noaa.gov/access/world-ocean-atlas-2023/).

**Base URL:**

```
https://noc-msm-o.s3-ext.jc.rl.ac.uk/ocean-obs/WOA23/
```

**Available Datasets:**

* WOA23_1971_2000_annual_climatology/
* WOA23_1971_2000_monthly_climatology/
* WOA23_1971_2000_seasonal_climatology/
* WOA23_1981_2010_annual_climatology/
* WOA23_1981_2010_monthly_climatology/
* WOA23_1981_2010_seasonal_climatology/
* WOA23_1991_2020_annual_climatology/
* WOA23_1991_2020_monthly_climatology/
* WOA23_1991_2020_seasonal_climatology/

### **Shelf Enabled NEMO**

We have also made a subset of the global eORCA025 (NEMO v4.0.4) Shelf Enabled NEMO (SE-NEMO) simulation available via the JASMIN cloud object store.

This 1/4° global ocean sea-ice simulation is forced by JRA55-do atmospheric forcing and initialised from EN.4.1.1 (1995-2014) initial conditions.

Monthly mean outputs defined on NEMO **T/U/V** points are available in version-controlled Icechunk repositories and can be accessed using `xarray.open_zarr()` as follows:

---

#### **NEMO Domain Data**

```python
import icechunk
import xarray as xr

# Define Icechunk storage:
storage = icechunk.s3_storage(
bucket="senemo-eorca025-jra55v1",
prefix="domain/domain_cfg",
region=None,
anonymous=True,
endpoint_url="https://noc-msm-o.s3-ext.jc.rl.ac.uk",
force_path_style=True,
)

# Open Icechunk repository & start read-only session on main branch:
repo = icechunk.Repository.open(storage=storage)
session = repo.readonly_session(branch="main")

# Open Icechunk store as xr.Dataset:
ds_domain = xr.open_zarr(session.store, consolidated=False)
ds_domain
```

#### **NEMO T/U/V Grid Data**

```python
# Define Icechunk storage:
storage = icechunk.s3_storage(
bucket="senemo-eorca025-jra55v1",
prefix="T1m", # "U1m" / "V1m" / "I1m"
region=None,
anonymous=True,
endpoint_url="https://noc-msm-o.s3-ext.jc.rl.ac.uk",
force_path_style=True,
)

# Open Icechunk repository & start read-only session on main branch:
repo = icechunk.Repository.open(storage=storage)
session = repo.readonly_session(branch="main")

# Open Icechunk store as xr.Dataset:
ds_senemo = xr.open_zarr(session.store, consolidated=False)
ds_senemo
```