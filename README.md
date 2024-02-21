# Drought Monitoring Using The Standardized Precipitation Index (SPI)

Author - Nitin Magima

Date - Feb 2024

Version - 1.0

The Standardized Precipitation Index (SPI) developed by McKee et al. (1993) describes the probability of variation from the normal precipitation over multiple years of data, on a monthly (or multiple months) time step. The SPI is calculated by taking the precipitation of the pixel i during timeframe j of year k minus the mean of pixel i during timeframe j over n years, divided by the standard deviation of pixel i during timeframe j over n years.

The aim of the jupyter notebook is to create a standardized precipitation index (SPI) timeline based on daily CHIRPS data (since 1981). The SPI is used as it highlights the difference to the mean precipitation during a given time and therefore provides information about drought-like conditions. The script will be executed within Google Earth Engine and will work on two independent SPI calculations. 

The first calculation deals with the "common" SPI, which is calculated on an n-months basis. A SPI, which is calculated for one month usually refers to the description of "SPI-1", for six months "SPI-6" and so on. The second SPI calculation is based on MODIS capture dates. As MODIS (MOD13Q1.006) provides information about the vegetation, it might be useful to compare its vegetation indices with the SPI. Therefore a 16-day SPI is calculated, whose start date matches with MODIS's start date (if the user does not apply a 'shift').

As precipitation data is usually not normally distributed, especially when it comes to timeframes of 12 months or less, a transformation should be applied. The data is typically fitted to a gamma function, but not supported in the script. The resulting SPI values can therefore just be used as an estimator.

Google Earth Engine (GEE) is a web-platform for cloud-based processing of remote sensing data on a large scale. The advantage lies in its remarkable computation speed as processing is outsourced to Google servers. The platform provides a variety of constantly updated datasets; no download of raw imagery is required. While it is free of charge, one still needs to activate access to Google Earth Engine with a valid Google account.


DISCLAIMER

This is a set of scripts  shared for educational purposes only.  Anyone who uses this code or its
functionality or structure, assumes full liability and credit the author.

Map Disclaimer

The designations employed and the presentation of the material on this map do not imply the expression 
of any opinion whatsoever on the part of the author concerning the legal status of any country, territory, city or area or of its authorities, or concerning the delimitation of its 
frontiers or boundaries.

Source
- [UN-SPIDER Knowledge Portal](https://www.un-spider.org/advisory-support/recommended-practices/recommended-practice-drought-monitoring-spi)