**Instructions for video_JSON_build.py**

Change following values according to video.

VIDEO_PATH = *path where zip files are place* for e.g. '/home/arian/aakash/10minVid/static/video1'

TOTAL_SEGMENTS = *Total number of segments of video* for e.g 300

TOTAL_BITRATES = *Total Number of bitrates available*  for e.g 5

properties['bitrates'] = *Bitrate values in bits per second in ascending order*
                        for e.g. [214915, 562660, 990946, 1520727, 2963872]
                        
properties['total_duration'] = *Total duration of segment* for e.g 600 

properties['duration'] = *Duration of each segment in second or millisecond* for e.g. 2000 

properties['timescale'] = *Timescale for segment duration, 1 for seconds, 1000 for milliseconds* for e.g. 1000


fileName = *Name template of zip files. $REPID$ will be replaced by corresponding bitrate index and $Number$ will be replaced by segment index* for e.g. 'video_$REPID$_dash$Number$.zip'

'video_0_dash7.zip' means 7th segment with minimum bitrate.

Tested with python 3.7

Saves video_properties.json in VIDEO_PATH folder.
