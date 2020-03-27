# NUS-CP3106
<b>AY 2019/2020 Semester II</b>.  
<b>By Yuxuan</b>.  
See report [here](NUS_CP3106_REPORT_YUXUAN.pdf).  
See video demo here.  

## Disclaimer
This work is an extension on Nguyen, Khanh, et al. “Vision-Based Navigation With Language-Based Assistance via Imitation Learning With Indirect Intervention.” <i>2019 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)</i>, 2019, doi:10.1109/cvpr.2019.01281. Github repo at https://github.com/debadeepta/vnla.

## To re-run our experiment
1) Clone the repo from the original work at <a href=https://github.com/debadeepta/vnla>here</a>  
2) Follow along the steps to:  
  a) <a href=https://github.com/debadeepta/vnla/tree/master/data>download data</a>.  
  b) <a href=https://github.com/debadeepta/vnla/tree/master/code>setup simulator</a>.  
3) After you are done, copy our [VNLA](VNLA) folder in this repo and overwrite to the orginal repo. Also add [verbal_qa_vocab.txt](asknav/verbal_qa_vocab.txt) to the corresponding folder of original repo.
```
$ cp -r VNLA root_dir/code/tasks/VNLA/
$ cp asknav/verbal_qa_vocab.txt root_dir/data/asknav/.
```
4) Run experients at root_dir/code/tasks/VNLA/scripts/
```
training:
$ bash train_main_results.sh [learned|none] [gpu id]
example: $ bash train_main_results.sh learned 0

evaluation:
$ bash eval_main_results.sh [learned|none] [seen|unseen]
example: $ bash eval_main_results.sh learned seen
```
   Note that parameters "random" and "first" in the original work are not implemented in our work, errors may be encountered
