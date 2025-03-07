---
title: Overview
description: Beta Features - Overview
---
<!-- the following links are referenced throughout this document -->

The beta features contains experimental features that we are working in progress but can be used by our users.
The services available in this section can be updated as we improve 

Currently, we are working in the following features:

[1]: #machines

## Machines

This product fetchs machine data from the providers (like JohnDeere, ClimateFieldView, CNHI) and store this data.
 
Currently, we are obtaining data from providers:
   * JohnDeere
   * CNHI

[2]: #prescriptions

## Prescriptions

This product organizes the data flow for prescriptions. For instance, the variable rate application can be done through prescription maps, which can be verified by the non-homogeneity of soil properties made in laboratory analysis. It is useful when applying lime, potassium and other products that can improve soil quality, applying only the amount needed for each area.

The prescription file is a zip file that should contain at least **three** files with the same name and specific extensions (**shp**, **dbf** and **shx**)

Our supported providers are:
* Raven Slingshot
* ClimateFieldView


[3]: #layers

## Layers

Layers is a product that will organize the information that is related to field and can be accessed a map.

Our supported providers are:
* [Sentera](https://blog.withleaf.io/en/senteraintegrationwithleaf).

[4]: #input

## Input

This feature will fetch, from operation files, varieties of crops harvested/planted and products applied and store this data.