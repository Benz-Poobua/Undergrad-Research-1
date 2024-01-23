# Undergraduate-Research-1
## Abstract
The Yakima Valley is located in the Columbia Plateau Regional Aquifer System (CPRAS). This area, which hosts around one-third of the state’s vineyards, is a very active agricultural area that depends on both surface and groundwater resources. The groundwater level has not been recorded in recent years. Additionally, the area’s shallow stratigraphy in the overburden strata (e.g., clay thickness), which contributes to the subsurface’s inelastic compaction, has not been fully studied. That leads to the question of the extent of the land subsidence of uplift due to the irrigation (i.e., groundwater use) that the Yakima Valley has experienced since 2017. Land subsidence was detected by Interferometric Synthetic Aperture Radar (InSAR) by Sentinel-1 from 2017 to 2022. MintPy algorithm and SBAS are utilized to select interferometric pairs and analyze the deformation time series. The InSAR time series reveals the Yakima Valley has experienced land subsidence of up to 10 cm since 2017. 
## Introduction
Yakima Valley (Fig. 1) is situated in south-central Washington in the Columbia Plateau Regional Aquifer System (CPRAS) and holds a position of paramount importance in the agricultural industry: around one-third of the state’s vineyards, including apples, pears, and concord grapes (“Yakima Valley AVA,” 2023; Burns et al., 2011; Norman et al., 2004; Nation, 2009). This region relies heavily on its local aquifers, along with the Yakima River, which bisects the appellation for irrigation water supplies (“Yakima Valley AVA,” 2023). 

The geological framework underlying Yakima Valley comprises the Columbia River Basalt Group (CRBG), which erupted between 17 and 5.5 Ma (Reidel et al., 2003), coupled with overlying basin-fill sediments or overburden. Overburden is deposits of undifferentiated unconsolidated to semi-consolidated sedimentary materials spanning from the Miocene to Holocene epochs (Burns et al., 2011). Burns et al. (2011) also modeled the thickness of the overburden unit, which revealed the presence of thick overburden strata within the valley.

A generalized geologic model has been established, which categorizes geological units within the region, including the overburden and five formations: Saddle Mountains Basalt, Mabton Interbed, Wanapum Basalt, Vantage Interbed, Grande Ronde Basalt, and Older Bedrock (Burns et al., 2011; Nation, 2009). As Amelung et al. (1999) suggested, clay thickness controls the extent and magnitude of subsidence for confined aquifers. However, the stratigraphy of the overburden is not studied or recorded thoroughly. 

The Yakima Valley resides within the Yakima Fold and Thrust Belt (YFTB), an ongoing deformation series of faults and folds spanning northern Oregon and south-central Washington. The folding and faulting of the basalt formations in the western part of the Columbia Basin, known as YFTB, originated concurrently with the CRBG eruptions. It has played a crucial role in shaping the topography of the Yakima Valley and the surrounding landscape (McCaffrey et al., 2016). Faults in the study area have the potential to act as a barrier to groundwater flow, leading to the partitioning of the aquifers. 

The limited data on crucial factors such as clay thickness, which significantly contributes to permanent land subsidence, and recent measurements of groundwater levels reflecting water usage in this agriculturally active area prompt essential questions. Is the Yakima Valley experiencing subsidence, uplift, or oscillation? Furthermore, do the observed deformations raise concerns among farmers or residents in the region?

 ![Alt text](https://github.com/Benz-Poobua/Undergraduate-Research-1/blob/main/AOI_yakima.png)
Figure 1. The Yakima Valley is the area of interest (AOI), represented by the red rectangle. This area is bounded by Ahtanum Ridge and Horse Heaven Hill Ridge.
## Methodology
We utilized Interferometric Synthetic Aperture Radar (InSAR) with the Sentinel-1 (C-band) satellite to detect land subsidence in the Yakima Valley. Data from 2017 to 2022 were gathered from ascending frames accessed through the Vertex Data Portal maintained by the Alaska SAR Facility (ASF). Two advanced algorithms were utilized for stacking and time-series analysis. The Short Baseline Subsets (SBAS) filter was employed to select interferogram pairs based on two criteria: a perpendicular baseline of less than 100 m and a temporal baseline ranging from 24 to 60 days, resulting in the selection of 153 interferogram pairs (Fig. 2). The Miami InSAR Time-series software in Python (MintPy) is an SBAS algorithm available through OpenSARlab, utilized for generating time series and conducting stacking within the designated area.

 ![Alt text](https://github.com/Benz-Poobua/Undergraduate-Research-1/blob/main/SBAS_yakima.png)
Figure 2. The interferogram pairs are selected using SBAS. 

After defining and downloading data for the study area, our initial step involved obtaining the UID and API key to access the Climate Data Store (CDS), which hosts a database of atmospheric pressure crucial for tropospheric delay correction. Following this, we established the reference point using MinPy's default approach, wherein the algorithm automatically selected a pixel with the highest spatial coherence in the stack. Subsequently, we performed an inversion to the small baseline network, enabling the calculation of the time series for the unwrapped phase. To refine the data, we corrected for the tropospheric delay from ERA5 and DEM errors, incorporating phase deramping to eliminate long-wavelength component noise. The detailed procedure of this algorithm (Fig. 3) was thoroughly documented by Yunjun et al. (2019). In the MinPy sign convention, negative phase values indicate subsidence, while positive values signify uplift.

![Alt text](https://github.com/Benz-Poobua/Undergraduate-Research-1/blob/main/minpy.png)
Figure 3. The algorithm of MinPy by Yunjun et al. (2019)
## Result
The time series of the line-of-sight (LOS) range change was derived from the preceding steps, revealing temporal variations in phase differences for 153 selected interferograms. A subset of these, showcasing both positive and negative LOS range change in the area, is available in the Supplementary Data section (Fig. S1-S7). These interferograms represent phase data from December 2016 to 2022, indicating dynamic changes in the region over time. The stacked interferogram (Fig. 4) visualizes the velocity in the line of sight (LOS) direction, highlighting an accumulated deformation in the Yakima Valley. Additionally, examining a particular point (46.40327, -120.46686) in the stacked interferogram reveals a linear trend (Fig. 5) in displacement with a velocity or slope of -1.43 cm/yr. Also, the graph indicates that the Yakima Valley has experienced accumulated deformation of up to 10 cm since 2017.

![Alt text](https://github.com/Benz-Poobua/Undergraduate-Research-1/blob/main/Stacking_yakima.png)
Figure 4. The stacked interferogram was obtained from the selected time frame. The Yakima Valley is decorrelated by agricultural activities. 

![Alt text](https://github.com/Benz-Poobua/Undergraduate-Research-1/blob/main/Trend_yakima.png)
Figure 5. The selected point (46.40327, -120.46686) displays the subsidence trend. For the sign convention, negative values mean the increase in range in the LOS direction. Positive values represent the decrease in range in the LOS direction. 
## Discussion
According to the sign convention, the Yakima Valley has exhibited subsidence of up to 10 cm since 2017. Furthermore, the distribution of the LOS displacement around the trend line (Fig. 5) suggests both uplift and subsidence, influenced by seasonal factors such as precipitation, discharge, and recharge time during the year. Interferograms in the region display decorrelation linked to agricultural activities, resulting in numerous missing pixels. Additionally, potential noise introduced by snow accumulation near Mt. Adams can impact interferogram quality.

The future project involves establishing a correlation between groundwater dynamics and ground deformation. However, crucial geotechnical data, including the stratigraphy of the shallow subsurface and groundwater levels in a time-series format, are currently unavailable. Detailed records of subsurface stratigraphy, particularly concerning factors like clay thickness, suggest the area's vulnerability to inelastic compaction, as observed by Amelung et al. (1999). Therefore, implementing groundwater level monitoring can help establish thresholds for irrigation use, preventing the region from groundwater overdraft and the associated risk of excessive stress on pre-consolidation stress.

## Conclusion
The Yakima Valley has experienced prolonged subsidence, up to 10 cm since 2017, as revealed by Sentinel-1 InSAR. Groundwater usage is suspected to be a contributing factor to this ground deformation. However, it is essential to gather supporting evidence, including data on groundwater levels and subsurface geology, to verify this claim. Consequently, the hypothesis suggesting permanent compaction in the Yakima Valley's subsurface remains inconclusive.

While the subsidence mechanism in the Yakima Valley remains unclear, the persistent nature of the subsidence signals a need for close monitoring of agricultural activities, particularly in vineyards. Further geotechnical surveys, including assessments of groundwater levels and shallow subsurface geology, are essential to understand the situation comprehensively. This approach will contribute to a more informed assessment of potential risks and mitigation strategies.

## Acknowledgement
I sincerely appreciate Professor David Schmidt (dasc@uw.edu) for his support throughout my research endeavor. Serving as my research supervisor, Prof. Schmidt has enriched my understanding of InSAR's theoretical complexities and shared insights and advice regarding the project, dataset, and data interpretation. His mentorship has played an essential role in shaping my research trajectory, and I am genuinely grateful for the opportunities to learn and develop under his guidance.

## References
Amelung, F., Galloway, D. L., Bell, J. W., Zebker, H. A., & Laczniak, R. J. (1999). Sensing the ups and downs of Las Vegas: InSAR reveals structural control of land subsidence and aquifer-system deformation. Geology, 27(6), 483-486.

Burns, E. R., Morgan, D. S., Peavler, R. S., & Kahle, S. C. (2011). Three-dimensional model of the geologic framework for the Columbia Plateau Regional Aquifer System, Idaho, Oregon, and Washington (No. 2010-5246). US Geological Survey.

McCaffrey, R., King, R. W., Wells, R. E., Lancaster, M., & Miller, M. M. (2016). Contemporary deformation in the Yakima fold and thrust belt estimated with GPS. Geophysical Journal International, 207(1), 1-11.

Nation, Y. (2009). Hydrogeologic framework of the Yakima River basin aquifer system, Washington.

Norman, D. K., Busacca, A. J., & Teissere, R. (2004). Geology of the Yakima Valley Wine Country--a Geologic Field Trip Guide from Stevenson to Zillah, Washington. Washington State Department of Natural Resources, Division of Geology and Earth Resources.

Reidel, S. P., Martin, B. S., & Petcovic, H. L. (2003). The Columbia River flood basalts and the Yakima fold belt.

Yakima Valley AVA. Washington State Wine Commission. (2023, September 8). https://www.washingtonwine.org/resource/yakima-valley-ava/ 

Yunjun, Zhang, Heresh Fattahi, and Falk Amelung. "Small baseline InSAR time series analysis: Unwrapping error correction and noise reduction." Computers & Geosciences 133 (2019): 104331.

