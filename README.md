# Flood Risk Management using Satellite Image Segmentation and Geospatial Analysis

During this year, there has been massive floods in Kerala and Nagaland costing the precious lives of thousands of beings and causing colossal damage. The frequency of hydrological catastrophes has been on the rise since the last few years. The idea is to manage the risks of flood neighbouring to the already flooded area and find better ways to save lives and prevent economic losses.
This is explained in this workflow as follows :-

- **Predict** -  
    * The topography of the terrain of all the prone areas(near water bodies) will be analysed using Digital Elevation Models(DEM).
    * DEM is 2D/3D representation of a terrain's surface, created from terrain elevation data.
    * A flood inundation model will be used to identify areas that will be impacted due to overflow of a water body.
    * This will allow to set up **alert stations and rescue forces base** at optimum positions in the possible area of disaster in the case of calamity.
    * Due to the optimum position of base stations, **a lot of lives can be saved and evacuation points** can be created to span the particular areas.
    
![Mercator Projection of DEM](https://github.com/kumar1202/code.fun.do/blob/master/predict/merc_projection.png "Mercator Projection of DEM")
![Flood Prediction](https://github.com/kumar1202/code.fun.do/blob/master/predict/flood_prediction.png "Flood Prediction")

- **Manage** - 
    *  In the case of a hydrological catastrophy, image segmentation will be used on live satellite feed of the affected area to determine the **remote and unserved areas** to setup distribution depots or drop packets.
    *  As there is no ground truth data for the model to train, so the before and after images of previous catastrophies will be used for clustering the image into segments.
    *  A convolutional autoencoder(also called as U-Net) will be used on the clustered satellite images to detect the flood affected areas in that terrain.
    *  The segmentation of the live feed can be deployed on any maps provider(like Google Maps) which will help in proper distribution of resources in crisis and in **identifying priority sites for rescue operations**.
