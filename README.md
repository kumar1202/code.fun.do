# Flood Risk Management using Satellite Image Segmentation and Geospatial Analysis

During this year, there's been massive floods in Kerala and Nagaland costing the precious lives of thousands of beings and causing colossal damage. The frequency of hydrological catastrophes has been on the rise since the last few years. The idea is to predict and manage the risks of flood in the affected areas and find better ways to save lives and prevent economic losses.

This is explained in this workflow as follows :-

- **Predict** -  
    * The first and essential procedure towards flood prediction is monitoring based on identifying the area most vulnerable to flooding, which    gives authorities relevant regions to focus.
    * The topography of the terrain of all the prone areas(near water bodies) will be analysed using Digital Elevation Models(DEM).
    * A flood inundation model will be used to identify areas that will be impacted due to overflow of a water body.
    * This will allow to set up **alert stations and rescue forces base** at optimum positions in the possible area of disaster in the case of calamity.
    * Due to the optimum position of base stations, **a lot of lives can be saved and evacuation points** can be created to span the particular areas.
    
![Mercator Projection of DEM](https://github.com/kumar1202/code.fun.do/blob/master/predict/merc_projection.png "Mercator Projection of DEM")

 >Fig. 1. Sample Mercator Projection of DEM
 
 ![Flood Prediction](https://github.com/kumar1202/code.fun.do/blob/master/predict/flood_prediction.png "Flood Prediction")
 
 >Fig. 2. Sample prediction of Flood using mercator projection


- **Manage** - 
    *  In the case of a hydrological catastrophy, image segmentation will be used on live satellite feed of the affected area to determine the **remote and unserved areas** to setup distribution depots or drop packets.
    *  As there is no ground truth data for the model to train, so the before and after images of previous catastrophies will be used for clustering the image into segments.
    *  A convolutional autoencoder(also called as U-Net) will be used on the clustered satellite images to detect the flood affected areas in that terrain.
    *  The segmentation of the live feed can be deployed on any maps provider(like Google Maps) will help in proper distribution of resources in crisis and in **identifying priority sites for rescue operations**.
![Flood Image Segmentation](https://github.com/kumar1202/code.fun.do/blob/master/manage/satellite_image_segmentation.png "Flood Image Segmentation")

>Fig. 3. Flood Image Segmentation 

## Operation

* The prediction stage will be active in normal period in order to strengthen the preparations to tackle any catastrophic events at its best with minimum loss.
* The management phase will be active in emergency period in order to provide relief in the most unserved and dangerous locations to minimize the impact of the disaster.
* The service can be deployed on any map provider that can be used by anyone to analyse the conditions of their areas and take proper personal actions, as well as the controlling offices to take right decisions.

## Datasets to be used

*  The DEMs(Digital Elevation Models) used for the prediction phase will be  CartoDEM provided by [Bhuvan](http://bhuvan.nrsc.gov.in/data/download/index.php), which is the Geoportal of Indian Space Research Organisation (ISRO) and provides various remote sensing datasets for India.
*  The satellite images for the management phase will be [OpenData](https://www.digitalglobe.com/opendata) which provides high quality RGB band images for before and after catastrophic events around the world.

## Technologies Used

- **TensorFlow** - An open-source software library for dataflow programming across a range of tasks to create deep learning models.
- **OpenCV** - OpenCV (Open Source Computer Vision) is a library of programming functions mainly aimed at real-time computer vision used for preprocessing images.
- **PyDEM** -  A package for topographic (terrain) analysis written in Python. It takes in digital elevation model (DEM) rasters, and it outputs quantities like slope, aspect, upstream area, and topographic wetness index.
- **GDAL** - A translator library for raster and vector geospatial data formats which  presents a single raster abstract data model and single vector abstract data model to the calling application.
