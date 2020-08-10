# Code for somatosensory input-specific behavioural output paper (Schorscher-Petcu et al). Control and acquisition software / code for analysis.


## Control and acquisition.vi

LabVIEW user interface for the control of optical stimulation and camera acquisition parameters.


## Local analysis.ipnyb

Used to process video files acquired with the high-speed infrared camera and to analyse changes in NIR-FTIR signal that reflect movement of the paw on the floor. It consists of the following main functions:

   1.	local_roi: creates a circular region of interest of defined radius centred on the video and extracts frame-wise mean intensity values from it. This function also calculates paw movement latencies based on a pre-defined threshold. 

   2.	roi_means_heatmap: creates a heatmap of mean intensity time-series for multiple trials.

   3.	local_motion_energy: calculates motion energy for each input file and transforms it into a video output. 

   4.	local_response_maps: computes pixel-wise response latencies and visualizes them as (i) a temporal map and (ii) a pixel-latency video.


## Global motion energy analysis.ipnyb

Code used to calculate motion energy from video files capturing the below-view of the whole stimulation platform. For each video, the code identifies the mouse being stimulated and isolates the corresponding chamber based on user-defined chamber coordinates. Frame-wise motion energy reflecting whole-body movements is calculated as an absolute value or as a binary expression based on a user-defined threshold. 

This is performed by a single main function called global_motion_energy, whoch identifies the experimental chamber in which stimulation occurred and calculates whole-body motion energy. Returns (i) frame-wise pixel difference values and (ii) a motion energy video.
