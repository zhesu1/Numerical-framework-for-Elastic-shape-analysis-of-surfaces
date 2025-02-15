# elasticMetrics

Tools for geometric shape analysis of spherical surfaces with first order elastic metrics based on the work by Martin Bauer, Eric Klassen, Hamid Laga, Stephen C. Preston and Zhe Su.

## What is it?

This code provides tools for geometric shape analysis on spherical surfaces with first order elastic metrics. 
It is able to factor out reparametrizations, translations and rotations. The following are two examples of geodesics between unparametrized surfaces presented in the paper "[Shape Analysis of Surfaces Using General Elastic Metrics](https://arxiv.org/abs/1910.02045)".

<img align="left" src="https://github.com/zhesu1/Figures/raw/master/registeredcat12_geo_unpara_1_1_-1_0_deg7_degv7_T13.png" width="800"><br clear="both"/> 

<img align="left" src="https://github.com/zhesu1/Figures/raw/master/registeredhorse02_geo_unpara_1_1_-1_0_deg7_degv7_T13.png" width="790"><br clear="both"/>

For details we refer to our papers

```css
@article{bauer2021oneforms,
	title={A diffeomorphism-invariant metric on the space of vector-valued one-forms},
	author={Martin Bauer, Eric Klassen, Stephen C. Preston and Zhe Su},
	journal={Pure and Applied Mathematics Quarterly},
	volume={17},
	number={1},
	pages={141-–183},
	year={2021}
}

@article{su2020shape,
  title={Shape analysis of surfaces using general elastic metrics},
  author={Su, Zhe and Bauer, Martin and Preston, Stephen C and Laga, Hamid and Klassen, Eric},
  journal={Journal of Mathematical Imaging and Vision},
  volume={62},
  pages={1087--1106},
  year={2020},
  publisher={Springer}
}
```

If you use our code in your work please cite our papers.

## Packages

Please install the following packages

* Pytorch: [https://pytorch.org/](https://pytorch.org/)
* Numpy: [https://numpy.org/](https://numpy.org/)
* Scipy: [https://www.scipy.org/](https://www.scipy.org/)
* Mayavi (for plotting): [https://docs.enthought.com/mayavi/mayavi/](https://docs.enthought.com/mayavi/mayavi/)

The code was tested on jupyter notebook.

## Shape Data

The datasets in the folder "ShapeData" are obtained from [http://tosca.cs.technion.ac.il/book/resources_data.html](http://tosca.cs.technion.ac.il/book/resources_data.html) and parametrized using the implementation provided in the following paper by Kurtek et al:
```css
@inproceedings{kurtek2013landmark,
  title={Landmark-guided elastic shape analysis of spherically-parameterized surfaces},
  author={Kurtek, Sebastian and Srivastava, Anuj and Klassen, Eric and Laga, Hamid},
  booktitle={Computer graphics forum},
  volume={32},
  number={2pt4},
  pages={429--438},
  year={2013},
  organization={Wiley Online Library}
}
```

## Usage

See the files "Calculate_geodesic_para", "Calculate_geodesic_unpara" and "Calculate_geodesic_unparaModSO3" for examples of how to use the code. Each surface should be represented using spherical coordinates as a function f:[0, &pi;] x [0, 2&pi;] &rarr; R<sup>3</sup> 
such that f(0, &theta;) = f(0, 0), f(&pi;, &theta;) = f(&pi;, 0) and f(&phi;, 0) = f(&phi;, 2&pi;). The code can be used directly for surfaces with resolution 50 x 99 (the numbers of discrete polar and azimuthal angles) since the corresponding bases are preloaded in the folder "Bases".  For the other resolutions, one can resample the surfaces or generate the corresponding bases for surfaces using the files in the folder "generateBases" and then put the bases files in the folder "Bases". 

## License

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see [http://www.gnu.org/licenses/](http://www.gnu.org/licenses/)

## Contacts

* Martin Bauer (bauer at math dot fsu dot edu)
* Zhe Su (zsu at math dot fsu dot edu)
