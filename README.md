## Introduction

This is the raw EEG data used in: 
Rutiku, R., Fiscone, C., Massimini, M., & Sarasso, S. (2024). Assessing mismatch negativity (MMN) and P3b within‐individual sensitivity — A comparison between the local–global paradigm and two specialized oddball sequences. European Journal of Neuroscience, 59(5), 842-859.

### What's in this dataset

Each participant (n=15) completed three different auditory oddball sequences: the Optimum-1 for MMN, the learning-oddball for P3b, and the local–global paradigm for the local and global effect. The tasks are formatted as different sessions but they were all recorded consecutively within one EEG experiment (order differed between participants). The local-global sequence was recorded in two separate EEG files (except for participant 5; see below for exception notes). Note that whereas the .vmrk files contain the original triggers for each recording, the _events files contain the correct event samples used in the analysis (in the fieldtrip cfg.trl format). It namely sometimes happened that some triggers were skipped by the recording system and these triggers needed to be interpolated using the event timestamps from the psychtoolbox output that was used to run the stimulation sequence (see below). Note also that the local-global sequence contains triggers for every single sound, but trials should be cut only for the first sound of every quintlet. The _events files already take that into account. 

| Subject | Session      | Run   |
| ------- |--------------|-------|  
| sub-01  | ses-MMN      |       | 
| sub-01  | ses-P3b      |       |
| sub-01  | ses-LGeffect | run-1 |
| sub-01  | ses-LGeffect | run-2 | 


### Auditory stimulation specs

The stimulation sequence information is provided in the original .mat format in the sourcedata folder. 
There are two files for each sequence: a file containing the sound definitions (_stimulation_SEQUENCE) and a file containing the timestamps for each sound (_critical_events).
The code used to run these sequences is included in the paradigms folder. 


### Exceptions

Participant 13 was recorded with 5000 Hz EEG sampling rate whereas all other participants were recorded with 2500 Hz EEG sampling rate. 
Participants 13, 14, and 15 were recorded chronologically first and they have slightly more trials for the oddball sequences. After inspecting their data, it was decided that trial numbers can be reduced for the rest of the participants in order to keep the recording time as short as possible while still having good sensitivity for the effects of interest. 
Participant 5 has three runs for the local-global task due to a need for an extra break by the participant. 
