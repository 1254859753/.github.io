# Introduction to  Address Graph  
This work unscrambles the characteristics of relative concepts, designs a graph structure and identifies modelling strategies. It proposes a schema on how to perform address matching and toponym disambiguation using an address graph.

## Table of Contents
- Homepage
- Demos
  - Demo 1
  - Demo 2
- Features
- Usage
  - Data
  - Code
- License

## Homepage
Please refer to the data URL.

Figshare:
- https://figshare.com/s/b32aaa0c2d152ecae01f
## Demo
- **Demo 1: Address Graph in Neo4j**
<img src=https://github.com/1254859753/1254859753.github.io/blob/6b4f301965beafe5358f5086b8b9ccd69b9240e3/%E5%9C%B0%E5%9D%80%E5%9B%BEneo4j.jpg width=60% />

- **Demo 2: The center node representing an address component**
<img src=https://github.com/1254859753/1254859753.github.io/blob/6b4f301965beafe5358f5086b8b9ccd69b9240e3/%E7%A6%8F%E7%94%B0%E5%8C%BA.JPG width=60% />

## Features
- **1. Different relations connection**
- **2. Supporting simple and fuzzy address macthing**
- **3. Supporting toponym disambiguation**

## Usage
### Data
-  **Administrative division data**

(corresponding section: Section 4)

The data are a sample of Chinese administrative divisions, which are used in the toponym **disambiguation task**. Limited by the national policy, only **<Nanjing City, JiangSu Province>** is provided. 

In the **China-Nanjing.xlsx** file, each column represents a data record referring to a specific administrative division. The **name** field is used to create **has_component** relations in the address graph. 

-  **Graph data**

(corresponding section: Section 3)

The **Edge** and **Node** directories store the basic node and edge files that can be imported into the graph database through a "Load csv" command. The name of the file is the types of nodes and edges. Generally, we first import node files and then edge files.

**Address.csv** is a complete preparing file to generate node and edge files in the project. In the file, **address segmentation** has been provided according to our semiautomatic method. We hope that the offered address segmentation can support more applications. 

-  **Matching data**

(corresponding section: Section 4)

The **Address-Different Type** file is used in the **address matching** task. It provides the queried address with different changed formats. The data can be reused to test fuzzy matching.

The **Address-Different Length** file is used in the **address matching** task. It provides the queried address with different string lengths.
 
### Code
-  **PythonPro_AMatching**
-  
(corresponding section: Section 4)

The project code is a prototype demo of address matching based on an address graph including for the original format and changed format. The **main.py** is the entrance of all projects. Simply copy the directory into a new project **PyCharm**, prepare the required **pylib**, then test the different addresses in the **Matching data**.

## License

Copyright © 2022 Address Graph Builder.
This project is MIT licensed.
