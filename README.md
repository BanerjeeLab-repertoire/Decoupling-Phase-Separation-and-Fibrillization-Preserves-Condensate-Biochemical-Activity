# Decoupling-Phase-Separation-and-Fibrillization-Preserves-Activity-of-Biomolecular-Condensates
The repository contains the codes used for processing and analyzing data for the paper - "Decoupling Phase Separation and Fibrillization Preserves Condensate  Biochemical Activity".

# Software 1: Fiji ImageJ v1.54f

# System requirements

Windows XP, Vista, 7, 8, 10, 11, etc.
Mac OS X 10.8 “Mountain Lion” or later
Linux on amd64 and x86 architectures

# Installation guide

You do not have to run an installer as Fiji is distributed as a portable application; just download, unpack, and start it using the application icon.

# Software 2: Anaconda distribution v2024.10-1

# System requirements

Windows 10 or later, 64-bit macOS 10.15+ (for Intel) or 64-bit macOS 11.1+ (for Apple Silicon), or Linux, including Ubuntu, RedHat, CentOS 7+, and others.

# Installation guide

1. Download the installer from the Anaconda website
2. Go to your Downloads folder (or Home folder if downloaded via CLI) and double-click the installer to launch.
3. Click Next and then agree to Anaconda’s Terms of Service (TOS).
4. Select an installation option - Just me/ All users
5. Click Next.
6. Select a destination folder to install Anaconda, then click Next.
7. Click Install. The installation might take a few minutes to complete. Click Show details to view the packages being installed.
8. Click Next twice, then click Finish to close the installer.

# Demo

# For the determination of the mean square displacement (MSD) of the beads inside the condensate system, follow the steps below;
1. Open the video (1000 frames acquired with 100 ms exposure time) provided in the folder /Data set/MSD determination folder using Fiji
2. Use TrackMate under the tracking plugin in Fiji to track the beads using the following steps
	(a) Provide the appropriate blob size (200 nm) and the image resolution (1 px=0.069 μm) as input parameters for tracking
	(b) Use the quality and intensity filters to avoid tracking aggregated beads
	(c) Export the bead trajectories as .xml files

3. Launch the Jupyter notebook using Anaconda Navigator
4. In the Jupyter notebook, open the custom Python codes - "Video particle tracking nanorheology.ipynb" from the folder - \Code and software\Python codes
5. Run the code by providing the .xml file as input, which was generated as the output from step 2. For convenience, the output file from step 2, named "Bead trajectories after tracking using Fiji," is also provided in the folder - \Data set\MSD determination. 
The codes can also be run directly on the .xml file provided.

# Expected outcome
MSDs of the beads tracked in the condensates. The codes also allow you to estimate the viscosity of the condensate microenvironment.

# For estimation of the complex moduli from MSDs 
1. Open the custom Python codes - "Determination of complex moduli from MSDs using Evans method.ipynb" in the Jupyter notebook from the folder - \Code and software\Python codes 
2. The .xml file provided in the folder - /Data set/Complex moduli determination should be used as an input by providing the address of the file in the code

# Expected outcome 
Complex moduli (Storage and loss moduli)

# Expected run time for demo on a "normal" desktop computer
For the entire demo (both MSD determination and estimation of complex moduli), it should take ~10 minutes. 

# Instructions for use - Videos acquired with known acquisition parameters (number of frames and exposure time) can be processed to get the particle trajectory data using Fiji. The custom python codes can be used on trajectory data 
with the input file format .xml to compute the particle MSDs and the complex moduli from the estimated MSDs.


