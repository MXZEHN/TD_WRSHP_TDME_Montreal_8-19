# TD_WRSHP_TDME_Montral_8-19
 The Post-AME-Encoder Presentation TD Summit 2019


IDEA:
This component is a proof of concept for a TouchDesigner based Media Encoder that integrates into an Adobe After Effects workflow. The idea is that you can render into TD supported codecs directly from AE. The idea was born when Adobe dropped support for the popular HAP codecs. However in the meantime it is possible again to encode HAP files with the Adobe Media Encoder and there is a very accomplished Batch Video Encoder for Touchdesigner - which means there is not so much use for this component anymore. However you may still find it useful, not only to render from After Effects but also to encode Videofiles from directories with image sequences.

PROCESS:
First it is necessary to install the TD_Encode presets to After Effects.
You can finde the necessary files in the /Presets folder. When you use the presets and tell AE to render into that watchfolder, the TD_Encode component will be able to tell from the folder name, how long the file will be, which framerate to apply and to which codec it should be encoded. 

<image>

Secondly you need to start the TD_Encode Component and point it to a watchfolder.
TD will recognise that new frames are coming in and encode them into a moviefile.
The output movie file will be placed next to the folder with the temporary frames.

OPTIONS:
Obviously you will need lots of free disk space to encode files that way. To help with this there is
the "destructive mode", which can be turned on in the component. With this enabled, TD will encode packages of 20 frames, stop the encoding, delete the already encoded files and continue with the next batch of 20.
This is obviously a bit dangerous and has to be used with care...
