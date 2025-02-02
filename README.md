# PyAMS version 2021
Python Antenna Measurement System is an open source framework for antenna measurement using ATS800B system

Version 1.0.1, November, 2021

Author: Omar Bouchenak Khelladi, Fabien Ferrero and Lionel Tombakdjian

ATS800B is provided by Rohde & Scharz company   
https://www.rohde-schwarz.com/de/produkt/ats800b-produkt-startseite_63493-642314.html?change_c=true

# ATS800B

The ATS800B system is based on a compact antenna test range (CATR) using a paraboloid reflector with a dualpolarization feed antenna placed at its single focal point to
transform a spherical wavefront into a planar wave distribution and vice versa.
With the compact dimension, the measurement system can stand on a bench lab bench, enabling radiation measurement at millimeter waves in a user-friendly environment.
The compact range has been designed for optimal operation in the 20-50GHz bands.
A rotational stage from PI motor is available to rotate the Antenna Under Test (AUT) during measurement.
The reflector source is a dual-port wideband Vivaldi that can capture two orthogonal polarizations simultaneously.
One objective of this repo will be to provide know-how to extend the capabilities of the actual system.

<img src="https://github.com/FabienFerrero/PyAMS/blob/main/Documents/pictures/setup.png">

# Measurement Equipments for antenna measurement

The optimal equipment to measure antenna with AT800B is a Vector Network Analyser. We are using a two ports ZNA67 with external connector option.

In order to measure the two components of the radiating wave using the two-feed of the recflector source, two different configurations must be use for AUT transmission or reception mode.

For testing your AUT in receiving mode, the required configuration is :
* The two ports of the refector source are connected to VNA port 1 et 2
* The AUT cable is connected to receiver B

<img src="https://github.com/FabienFerrero/PyAMS/blob/main/Documents/pictures/schematic_Rx.png">

For testing your AUT in transmission mode, the required configuration is :
* The two ports of the refector source are connected to receiver R2 and B
* The AUT cable is connected to Port 1

<img src="https://github.com/FabienFerrero/PyAMS/blob/main/Documents/pictures/schematic_Tx.png">


# How to install

PyAMS will require several Python lib :
- Math
- Numpy
- Matplotlib
- Time
- RsInstrument ( for R&S VNA)
- pipython (lib from PI motor)
- MBX Python Library (path: ```C:\SWMilliBox\MBX\python\```)

# Example of measurement

We recently measure a  28GHz switched beam lens antenna.
The switched matrix and Vivaldi antenna array are provided by EV Technologie. 
The matrix can connect any of the 4 input ports and any of the 16 output ports up to 30GHz.

<img src="https://github.com/FabienFerrero/PyAMS/blob/main/Documents/pictures/1636896716788.jpg">

# REFERENCES

ATS800B, accessed June, 2020. [Online].Available:
[https://scdn.rohde-schwarz.com/ur/pws/dl_downloads/dl_common_library/dl_brochures_and_datasheets/pdf_1/ATS800B_dat-sw_en_3607-9572-22_v0100.pdf]
