ALPHA 2.5: Frostbite Revival (Released 12/23/21)

Changelog:

    [ UI ] Chained design. All steps link to one another! Use the master override toggles to skip processes.
    [ Upscaling ] GFPGAN face-enhance toggle (embedded in Real-ESRGAN)
    [ Interpolation ] Practical-RIFE implementation; 4.0 model
    [ File mgmt ] Compatibility with padded filenames, File overwrite protection, verification of completion
    [ Misc ] Forked essential dependencies for long-term backwards compatibility; if needed.

*This updates brings AnKit back to a functioning state. Upcoming updates will make use of recent prerequisite updates and coinciding AI advances. *

---

# AnimationKit - AI Upscaling & Interpolation using Real-ESRGAN+RIFE
*Your (eventual) all-in-one AI post-processing tool!*

*Early Alpha Google Colab Notebook*

1. [AnimationKit Colab Notebook](https://github.com/patrickabadi/AnimationKit-AI/blob/main/AnimationKit_Rife_RealESRGAN_Upscaling_Interpolation.ipynb) for Real-ESRGAN <a href="https://colab.research.google.com/github/patrickabadi/AnimationKit-AI/blob/main/AnimationKit_Rife_RealESRGAN_Upscaling_Interpolation.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="google colab logo"></a>.


Features:
- :white_check_mark: Real-ESRGAN video upscaling (Raise your resolution by up to 4x!)
- :white_check_mark: Practical-RIFE motion smoothing / video interpolation (Make choppy footage smooth)
- :white_check_mark: Chained design - No need to sort through multiple cells! Set your options and forget it.
- :white_check_mark: Google Colab (with basic UI) & Google Drive support
- :white_check_mark: Import either mp4 files or an individual frame folder

Real-ESRGAN video upscaling, RIFE interpolation/motion smoothing, and FFMPEG hevc_nvenc (h265) compression

---

Credits: Motion smoothing conceived from "Zoom animation processing and motion interpolation" added by https://twitter.com/unltd_dream_co. This part of the script uses [RIFE real-time video interpolation](https://github.com/hzwer/arXiv2020-RIFE) to smooth out the resulting video. 

Upscaling uses Real-ESRGAN (https://github.com/xinntao/Real-ESRGAN). A demo notebook for static images can be found here: https://colab.research.google.com/drive/1k2Zod6kSHEvraybHl50Lys0LerhyTMCo?usp=sharing. The demo was based on the following paper: [''Real-ESRGAN: Training Real-World Blind Super-Resolution with Pure Synthetic Data''](https://arxiv.org/abs/2107.10833).

<img src="https://raw.githubusercontent.com/xinntao/Real-ESRGAN/master/assets/teaser.jpg" width="100%">



Feature additions & bugfixes:

---


Feel free to report bugs and/or help with developments! See the "Issues" page for documentation and development notes-

#Prior Changelog (Incomplete)

##ALPHA 2: Released 9/4/21
Feature additions
- :🔻: Deflickering [Depcrecated]
- :white_check_mark: Upscaling from individual frames (P2)
- :white_check_mark: Target length (in seconds) for RIFE interpolation - Replaces old length_multiplier option


#Alpha 1 release: All major bugs have (hopefully) been patched. New functions will be released in the testing branch until debugged.
- :white_check_mark: Anime model for realesrgan
- :white_check_mark: 2x model
- :white_check_mark: target output path
- :white_check_mark: omission of outscaling (note, may need to check defaults in inference.py)
- :white_check_mark: target fps no longer causes duplicates prior to ffmpeg end-phase (prevents upscaler from wasting gpu cycles on duplicate frames; major speed increase)
- :white_check_mark: notebook set to high memory - necessary for RIFE
