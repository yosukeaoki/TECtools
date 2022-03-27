# TECtools
Tools to compute Total Electron Contents from GNSS data

## rdrnx3.f 

A fortran program to read a RINEX3 file to obtain Slant Total Electron Content (STEC). Originally written by Prof. Kosuke Heki (Hokkaido University) for RINEX2 files. 

### Compilation 

% gfortran -o rdrnx3 rdrnx3.f

### Usage 

% rdrnx3 [RINEX file] [Satellite] [Start UTC (hr)] [End UTC (hr)] >! [Output file] 

  Satellite: G = GPS, R = GLONASS, J = QZSS

  e.g., rdrnx3 TSKB0010.22o G 3.0 8.0 >! STEC_GPS.dat

## rdeph3.f 

A fortran program to read a RINEX3 navigation file to obtain the satellite orbit. Originally written by Prof. Kosuke Heki (Hokkaido University) for RINEX2 files. 

### Compilation 

% gfortran -o rdeph3 rdeph3.f 

### Usage 

% rdeph3 < [RINEX file] >! [Output file]

  e.g., rdeph3 < TSKB0010.22n >! orb_GPS.dat
  
