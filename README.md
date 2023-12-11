# Undergraduate-Research-1
## Abstract
Yakima Valley, located in south-central Washington in the Columbia Plateau Regional Aquifer System (CPRAS), plays an essential role in agricultural activity: around one-third of the state’s vineyards. The area’s aquifer and land subsidence measurements have not been closely monitored or recorded in recent years. That leads to the question of the extent of the land subsidence of uplift due to the irrigation (i.e., groundwater use) and climate change (frequent droughts) that the Yakima Valley has experienced since 2017.  Land subsidence was detected by Interferometric Synthetic Aperture Radar (InSAR) by Sentinel-1 from 2017 to 2022. Minpy algorithm and SBAS are used to select interferometric pairs and analyze the deformation time series. The InSAR time series reveals the Yakima Valley has experienced land subsidence of up to 10 cm since 2017. The lithology in the area and the groundwater level measurements are encouraged to monitor the irrigation and determine the likelihood of the subsurface’s inelastic compaction.
## Introduction
Yakima Valley (Fig. 1) is situated in south-central Washington in the Columbia Plateau Regional Aquifer System (CPRAS) and holds a position of paramount importance in the agricultural industry: around one-third of the state’s vineyards (“Yakima Valley AVA,” 2023; Burns et al., 2011; Norman et al., 2004; Nation, 2009). This region relies heavily on its local aquifers, along with the Yakima River, which bisects the appellation for irrigation water supplies (“Yakima Valley AVA,” 2023). 

The geological framework underlying Yakima Valley comprises the Columbia River Basalt Group (CRBG), which erupted between 17 and 5.5 Ma (Reidel et al., 2003), coupled with overlying basin-fill sediments or overburden. Overburden is deposits of undifferentiated unconsolidated to semi-consolidated sedimentary materials spanning from the Miocene to Holocene epochs (Burns et al., 2011). Burns et al. (2011) also modeled the thickness of the overburden unit, which revealed the presence of significant, thick overburden strata within the valley.

A generalized geologic model has been established, which categorizes geological units within the region, including Overburden and five formations: Saddle Mountains Basalt, Mabton Interbed, Wanapum Basalt, Vantage Interbed, Grande Ronde Basalt, and Older Bedrock (Burns et al., 2011; Nation, 2009). As  ​​ Amelung et al. (1999) suggested, clay thickness controls the extent and magnitude of subsidence. However, the stratigraphy of the overburden is not studied or recorded thoroughly. 

Furthermore, Yakima Valley resides within the Yakima Fold and Thrust Belt (YFTB), an ongoing deformation series of faults and folds spanning northern Oregon and south-central Washington. The Folding and faulting of the basalt formations in the western part of the Columbia Basin, known as YFTB, originated concurrently with the CRGB eruptions. It has played a crucial role in shaping the topography of the Yakima Valley and the surrounding landscape (McCaffrey et al., 2016). Faults in the study area have the potential to act as a barrier to groundwater flow, leading to land subsidence. 

These considerations prompt the following questions: Is the Yakima Valley experiencing subsidence, uplift, or oscillation? And, do the observed deformations elicit concerns among farmers or residents in the region?

## Methodology
We employed InSAR with the Sentinel-1 (C-band) satellite to identify land subsidence in the Yakima Valley. Data from 2017 to 2022 was gathered from ascending frames accessed through We employed InSAR with the Sentinel-1 (C-band) satellite to identify land subsidence in the Yakima Valley. Data from 2017 to 2022 was gathered from ascending frames accessed through the Vertex Data Portal maintained by the Alaska SAR Facility (ASF). Two advanced algorithms were utilized for stacking and time-series analysis. The Short Baseline Subsets (SBAS) filter was employed to select interferogram pairs based on two criteria: a perpendicular baseline of less than 100 m and a temporal baseline ranging from 24 to 60 days, resulting in the selection of 153 interferogram pairs (Fig. 2). Additionally, the Miami INsar Time-series software in PYthon (MintPy) was employed to construct time series and perform stacking within the designated area. The procedure of this algorithm (Fig. 3) was thoroughly described by Yunjun et al. 2019, such as noise correction from atmospheric (tropospheric delay correction) artifacts or DEM corrections.

## Result





## Discussion






## Conclusion
The Yakima Valley has experienced prolonged subsidence, up to 10 cm since 2017, as revealed by Sentinel-1 InSAR. Groundwater usage is suspected to be a contributing factor to this ground deformation. However, it is essential to gather supporting evidence, including data on groundwater levels and subsurface geology, to verify this claim. Consequently, the hypothesis suggesting permanent compaction in the Yakima Valley's subsurface remains inconclusive.

While the subsidence mechanism in the Yakima Valley remains unclear, the persistent nature of the subsidence signals a need for close monitoring of agricultural activities, particularly in vineyards. Further geotechnical surveys, including assessments of groundwater levels and shallow subsurface geology, are essential to understand the situation comprehensively. This approach will contribute to a more informed assessment of potential risks and mitigation strategies.

