# mlalgos

A collection of (un)supervised Machine Learning (ML) Algorithms (MLA) and ML Tools for object detection and classification on satellite imagery.

Full documentation is hosted here: 

Installation is easy:

~~~
pip install mlalgos
~~~

MLAs are implemented using standard ML packages such as scikit-learn and tensorflow. 
MLAs also utilize open source libraries which can read from and write to georeferenced satellite images such as gdal.

The purpose of this repository is to enable fast prototyping of object detection and classification solutions employing
one of the existing algorithms or by constructing new ones based on the provided modular tools.

The input of a MLA is one or more of the following:

+ one or more images;
+ a job.json specifying the parameters of the MLA;
+ a train.geojson containing a collection of features, each feature consisting of (at least) a geometry, a class and a unique image identifier;
+ a target.geojson containing a collection of geometries, each feature consisting of (at least) a geometry, a class and a unique image identifier;

The output of a MLApp is one or more of the following:

+ one or more processed images
+ an output.geojson containing a collection of features, each feature consisting of (at least) a geometry, a class and a unique image identifier;

Imagery in the format required by a MLApp (e.g., pansharpened, multi-spectral or orthorectified) can be obtained with the gbdxtools package (https://github.com/kostasthebarbarian/gbdxtools). You need GBDX credentials to use gbdxtools.