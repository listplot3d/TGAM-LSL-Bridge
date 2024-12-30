# What is TGAM-LSL Bridge
a bridge to forward NeuroSky [TGAM](https://store.neurosky.com/products/eeg-tgam) data from BLE-USB Adaptor to [LSL](https://labstreaminglayer.org/) Stream
so data can be process with Open Source tools.

The positioning of TGAM_LSL Brdige in toolchain/topology used by me personally, is shown below:

![postion of TGAM-LSL Bridge](intro.png)

# How to Run
* turn on TGAM head band
* makde sure that your COM port specificied in NeuroSkyTGAM_LSLBridge.py, is identical to the one shown on PC
* run following command in src forder:

>python ./NeuroSkyTGAM_LSLBridge.py

Then you should be able to see output like this:
```
Started Stream: < sInfo 'TGAM EEG Stream' >
  | Type: EEG
  | Sampling: 512.0 Hz
  | Number of channels: 1
  | Data type: <class 'numpy.int16'>
  | Source: TGAM_to_LSL

* Established connection with COM5
* Started Forwarding COM data to Stream...
```
* then run following command, will see the output of Stream

> mne-lsl viewer



