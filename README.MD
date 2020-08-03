# FieLDS
Field Landscape Decision Support

Field Landscape Decision Support (FieLDS) is a decision support tool that assists agricultural producers 
and farm managers with selecting field segments that can be converted from corn and soybean commodity crops 
to bioenergy crops such as perennial grasses to meet producer’s priorities. Conversion recommendations are 
based on site-specific landscape properties. Using the tool, producers select priorities (i.e., sustainability 
indicators) that are most relevant to their decision-making and provide spatial [Geographic Information System (GIS)]
input for implementing those priorities. Based on each individual’s input, FieLDS generates a field layout and 
spatially marks where to place each type of plant. By allowing users to set weights among their priorities, the 
tool empowers them to generate field designs specific for their needs rather than those reflecting the developer, 
biorefinery, or government priorities, thus increasing transparency of the decision process.  


### Who is this tool for?

This tool is designed for agricultural producers and land managers who desire to plant alternative crops such as 
perennial grasses but are not sure where in the landscape they would fit best. Perennial grasses can be planted for 
sale to bioenergy markets, as animal bedding, for erosion control, or simply to improve water and soil quality and 
increase biodiversity. FieLDS is intended to assist producers with diverse priorities – increasing profitability, 
maintaining soil quality, preventing erosion, ensuring high water quality, and providing employment to enhance rural 
development. Each priority may be relevant to the producer, but to a different extent. The FieLDS tool allows users 
with different backgrounds and priorities tailor complex field designs to meet their specific needs.  

The decision support tool was designed based on interviews with agricultural producers. Those interviews generated a 
list of priorities (sustainability indicators) based on the frequency of discussion. Furthermore, each producer 
assigned a weight to each priority. Developers can add priorities and spatial inputs if the current list of 
sustainability indicators does not reflect all factors they consider relevant for decision-making. 

One of the main features of FieLDS is that it not only uses high-resolution spatial input to develop a field layout 
based on priorities, but also it uses a “smoothing” heuristic to ensure the resulting field designs are easily 
operable with current agricultural machinery. The “smoothing” process was implemented to avoid a fractured landscape 
created by only doing pixel-by-pixel comparisons between crop types. Such heuristic techniques were developed 
specifically for the tool, and are time-efficient and easy to implement in order to generate an operable field plan 
without requiring resource-intensive optimization calculations. 


### Inputs

To use FieLDS, a producer specifies the landscape area where the field is located. At first, they select priorities 
from a list of 15 indicators and assign relative weights (how important each indicator is) (Step 1 below). Next, 
based on the priorities selected, the user enters spatial inputs corresponding to those priorities (Step 2 below, 
an example of spatial input data for predicted perennial grass yield is illustrated in that stepI). Finally, if 
desired, users can adjust pre-set utility functions among the priorities (Step 3) as outlined below.

- 1.	*Producer priorities*. The tool is populated with 15 sustainability indicators that producers can choose among 
and assign weights, but if they are inadequate, new priorities can be added.
- 2.	*Farm information*. Relative to each priority affecting the farmer’s decision, farm-specific inputs would 
include spatial soil and water quality data, profitability goals, and any other relevant factor. Such datasets are available 
for the State of Iowa as part of the Sustainable Landscape Design Project. Upon request, those data layers can be provided 
to external users, although if the user is outside of Iowa, they will need to have their own spatial input data. Farm 
information can be input as either raster or vector files, which are converted to raster files. 
- 3.	The decision support tool has a set of utility functions for each sustainability indicator that are pre-set. 
If desired, users can modify the utility function or add more priorities/spatial inputs depending on the availability 
of information. 

### Documentation

In the attached GitHub folder, you will find Python code that can be used to process spatial inputs and generate a 
landscape layout. The document is intended for a technical audience because it does not contain a Graphical User 
Interface (GUI) but rather presents the actual code for spatial analysis. The code might be changed in the future 
as more optimization features are added to the tool. 

### Technical details

The developed code references several Python libraries. Spatial data were processed using Python 3.6.9 language in 
Jupyter Notebook (https://jupyter.org/) with Geographic Information Systems (GIS) processing packages for spatial 
data processing: rasterio 1.0.21, pandas 0.25.3, geopandas 0.4.1, matplotlib 3.1.1., georasters 0.5.15 and numpy 1.17.4.

### Outputs

What can you expect from using the tool? FieLDS will generate a field layout with suggested placement of annual and 
perennial crops. Tangible benefits from using the tool and proposed crop layouts include helping farmers and 
landowners understand where perennial grasses would best fit within their individual fields. Adopting the recommendations 
would potentially improve farm profitability, diversify agricultural production, improve water and soil quality, 
and provide better habitat for wildlife. If the grass is harvested, it can serve as feedstock for bioenergy or biomaterials. 
 
### Other Software
Idaho National Laboratory is a cutting edge research facility which is a constantly producing high quality research 
and software. Feel free to take a look at our other software and scientific offerings at:

[Primary Technology Offerings Page](https://www.inl.gov/inl-initiatives/technology-deployment)

[Supported Open Source Software](https://github.com/idaholab)

[Raw Experiment Open Source Software](https://github.com/IdahoLabResearch)

[Unsupported Open Source Software](https://github.com/IdahoLabCuttingBoard)

### License

Copyright 2020 Battelle Energy Alliance, LLC

Licensed under the MIT (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

  https://opensource.org/licenses/MIT

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.




Licensing
-----
This software is licensed under the terms you may find in the file named "LICENSE" in this directory.