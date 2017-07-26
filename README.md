# 3D MicroG, Computational Thermal & Fluid Dynamics Laboratory Micro-Gravity Metal FDM
Micro-gravity [Metal Fused Deposition Modeling](https://github.com/nolanholden/3d-micro-g/blob/4fd37d409fcfca17d81ec334c00d76ba0316be27/docs/fused-deposition-modeling-of-metals.pdf) (3D metal printing) NASA payload for [Blue Origin](https://www.blueorigin.com/), with the [University of Louisville Computational Thermal & Fluid Dynamics Laboratory](http://yongshenglian.wixsite.com/ctflab).


# 3D MicroG Start-up Module

## Abstract
This document is provided as a rough outline of requirements and additional details for the design of the 3D Micro-G module responsible for detecting the host vehicle’s apogee and commencing FDM prints during the target time-interval of flight. The content is ordered as follows:
1. Definitions
2. Mission Timeline
3. ADDAM Requirements and Related Components
4. Enumeration of ADDAM Components


## 1. Definitions
- **APW (Apogee Printing-Window)** – the target interval of time after takeoff and before landing during which FDM print(s) are to be performed. (Roughly 5 minutes in length)
- **ADDAM (APM Detection and Data-Acquisition Module)** – the module (hardware and software) responsible for detecting the onset (and conclusion) of APW, commencing the FDM print(s), and acquiring various non-critical data throughout flight


## 2. Mission Timeline (rough)
1. Vehicle launches.
2. ADDAM begins sensing for APW onset (and begins all other data-acquisition capabilities.)
3. ADDAM detects APW onset.
   - ADDAM immediately commences FDM prints.
4. Prints finalize during APW.
5. APW ends.
6. Spacecraft returns to Earth


## 3. ADDAM Requirements and Related Components
- The ADDAM must, requiring no intervention, begin sensing for APW immediately upon power-on. (Power-on must occur prior to APW.)
  - Accelerometer to sense APW
- The ADDAM may also acquire various environment metrics:
  - Visible-light spectrum video
    - Visible light spectrum light
    - Visible light spectrum camera
  - Infrared video
    - Infrared camera
  - Magnetic field (potential magnetic interference)
    - Magnetometer
  - “Real-time” timekeeping
    - If module is primitive (and time is too unreliable), potentially should be an external clock.
  - Amperage to and voltage across printer (or entire system)
    - Electronically interfaceable ammeter and voltmeter
- Additional, Non-critical metrics
  - GPS NMEA sentences (altitude, UTC date-time, satellites tracking, etc.)
  - Ambient pressure
  - Ambient temperature (unless IR imaging suffices)
  - Relative humidity


## 4. Enumeration of ADDAM Components
##### Mission-critical:
- Power supply
- Accelerometer
##### Non-critical:
- Visible light spectrum light
- Visible light spectrum camera
- Infrared camera
- External clock
- Electronically interfaceable multimeter
##### Very low-importance
  - GPS receiver
  - Barometer
  - Thermometer
  - Hygrometer (humidity)

_For more information, please contact Nolan Holden at nolan.holden@louisville.edu._


---


## License Information

As expressed in [this repository's license](https://github.com/nolanholden/3d-micro-g/blob/master/LICENSE), The below terms are an addition to the GNU GPLv3, and all terms here which intersect those in GNU GPLv3 shall be entirely superceding:

All intellectual property accompanying this electronic document shall not be copied, distributed, or shared without prior written consent by its owner, Nolan Frederick Holden of the University of Louisville Speed School of Engineering, or by any team member under Dr. Yongsheng Lian (requiring written proof from Dr. Yongsheng Lian of involvement and his express permission to project resources), or by Dr. Yongsheng Lian himself. All intellectual property accompanying this electronic document is final property of its owner, Nolan Frederick Holden of the University of Louisville Speed School of Engineering, Dr. Yongsheng Lian's Computational Thermal & Fluid Dynamics Laboratory.

_For requests of permission, please contact Nolan Holden at nolan.holden@louisville.edu._
