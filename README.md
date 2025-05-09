# Rotman Lens Design in MATLAB with HFSS Port

The following repository is a "fork" of the [amazing codebase](https://www.mathworks.com/matlabcentral/fileexchange/50490-rotman-lens-design-with-hfss-link) designed by Dr. Michael Pokorny and Professor Zbynek Raida from the Brno University of Technology in the Czech Republic. This repository is in no way endorsed by the developers, and originates from their latest 15 NOV 2019 revision posted on the MATLAB File Exchange. 

Given that the last update was almost 6 years ago, there are some parts of this codebase that I find outdated. However, the true power this codebase offers in seamless Rotman lens design and a clever way to port over to HFSS should be maintained, in my opinion. As such, I felt it pertinent to move the code over to Github, where the open source community can help advance and maintain Pokorny and Raida's code. 

## Original Overview from the Developers

The design script generates a planar polygon with N vertices defined by coordinate vectors X and Y. Polygon represents the contour of the planar Rotman Lens (RL) based on the user-defined input parameters. RL port phase centers are obtained by the evaluation of the formulas published by Peter S. Simons, 2004. The HFSS link script modifies the coordinates of the already existing HFSS file containing an arbitrary planar polygon with N vertices. A multi-line tool may be used to create such polygon. Input ASCII file consists of N coordinates represented by X and Y vectors defining the contour of the planar Rotman Lens (RL). To get input file run design script first.

## System Requirements

The codebase as-is has been tested with MATLAB R2023a and AnsysEM 2024 R2. One of the main updates to this code that has been added is the transition from `.hfss` to `.aedt`, which supports AnsysEM years 2020 and beyond.

## Repository Usage

Documentation is available in the appropriate directory in this repository. However, a very easy way to get up and running quickly is:

1. Clone this repository:
```bash
git clone https://github.com/mosa11aei/matlab-hfss-rotman.git
```
2. Open `RLpolygon_v1_1.m`, and modify your lens parameters as necessary. Run this code in its entirety.
3. Open `HFSSFile.m`. Make sure your output directory, and HFSS template, are entered. Run this code in its entirety.
4. You now have a `.hfss` (or `.aedt`) file which you can open in AnsysEM to work with. 
5. [This video](https://www.youtube.com/watch?v=DeG8BaYmvpw) describes the process well in advancing the design to model EM characteristics of the lens.

## Citation

Please cite the original developers, but you may link to this version of the code. A `CITATION.cff` is provided for easy citation generation.