# TD_WRSHP_TDME_Montral_8-19
 The Post-AME-Encoder Presentation TD Summit 2019


IDEA:
This component is a proof of concept for a TouchDesigner based Media Encoder that integrates into an Adobe After Effects workflow. The idea is that you can render into TD supported codecs directly from AE. The idea was born when Adobe dropped support for the popular HAP codecs. However in the meantime it is possible again to encode HAP files with the Adobe Media Encoder and there is a very accomplished Batch Video Encoder for Touchdesigner by VT Pro Design(https://chopchopchop.org/assets/applications/batch-video-converter) - which means there is not much use for this component anymore. However you may still find it useful, not only to render from After Effects but also to encode videofiles from directories with image sequences.

PROCESS:
First it is necessary to install the TD_Encode presets to After Effects.
You can finde the necessary files in the /Presets folder. Then you tell AE to render into a watchfolder: The TD_Encoder component watching that folder will be able to tell from the folder name, how long the file will be, which framerate to apply and to which codec it should be encoded.
!! In the filename you can not use underscores "_" and spaces" " !! 

Secondly you need to start the TD_Encode Component and point it to that watchfolder.
TD will recognise when new frames are coming in and start to encode them into a moviefile.
The output movie file will be placed next to the folder with the temporary frames, which will be deleted by the time the movie has been finished.

DISCLAIMER:
This is nor a production tool, but a workshop/tutorial demo file - work in progress! 

