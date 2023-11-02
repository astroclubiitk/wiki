---
title: AstroQuery
layout: default
parent: MAST
grand_parent: Astrophotography
nav_order: 2
---

## AstroQuery

<br />
[AstroQuery]() is a python package that can be installed using:

```sh
pip install astroquery
```

AstroQuery's [`astroquery.mast`](https://astroquery.readthedocs.io/en/latest/mast/mast.html) is a module that can be used to query and access data in the [MAST](.) archive.

It offers 3 main services:

1. [MastClass](https://astroquery.readthedocs.io/en/latest/api/astroquery.mast.MastClass.html#astroquery.mast.MastClass): Allows direct programatic access to the [MAST](.) portal. Along with [ObservationsClass](https://astroquery.readthedocs.io/en/latest/api/astroquery.mast.ObservationsClass.html#astroquery.mast.ObservationsClass), it is used to query MAST observational data.
2. [CatalogsClass](https://astroquery.readthedocs.io/en/latest/api/astroquery.mast.CatalogsClass.html#astroquery.mast.CatalogsClass): Used to query MAST calalog data. The available catalogs include the Pan-STARRS and Hubble Source catalogs along with a few others.
3. [Cutouts](https://astroquery.readthedocs.io/en/latest/mast/mast_cut.html): A newer addition to `astroquery.mast`, it provides access to full-frame image cutouts of [Transiting Exoplanet Survey Satellite (TESS)](https://tess.mit.edu/), MAST Hubble Advanced Product (HAP) and deep-field images, through [TesscutClass](https://astroquery.readthedocs.io/en/latest/mast/mast_cut.html#tesscut), [HapcutClass](https://astroquery.readthedocs.io/en/latest/mast/mast_cut.html#hapcut) and [ZcutClass](https://astroquery.readthedocs.io/en/latest/mast/mast_cut.html#zcut) respectively.

Other than this, you can also access [MAST](.) data using the MAST API. Read the [documentation](https://mast.stsci.edu/api/v0/) for more information.
