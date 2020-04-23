# NUS-CP3106
<b>AY 2019/2020 Semester II</b>.  
<b>By Yuxuan</b>.  
See report [here](NUS_CP3106_REPORT_YUXUAN.pdf).  
See video demo [here](https://youtu.be/E7eLIXqEhCQ).  

## Disclaimer
This work is an extension on Nguyen, Khanh, et al. “Vision-Based Navigation With Language-Based Assistance via Imitation Learning With Indirect Intervention.” <i>2019 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)</i>, 2019, doi:10.1109/cvpr.2019.01281. Github repo at https://github.com/debadeepta/vnla.

## To re-run our experiment
1) Clone the repo from the original work at [here](https://github.com/debadeepta/vnla).  
2) Follow along the steps to:  
  a) [download data](https://github.com/debadeepta/vnla/tree/master/data).  
  b) [setup simulator](https://github.com/debadeepta/vnla/tree/master/code).   
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
$ bash eval_main_results.sh [learned|none] [seen|unseen] [gpu id]
example: $ bash eval_main_results.sh learned seen

no room experiment:
$ bash train_noroom.sh noroom_learned [gpu id]
$ bash eval_noroom.sh noroom_learned [seen|unseen]
```
Note that baselines "random" and "first" in the original work are not implemented in our work, errors may be encountered. Rule ablation study is also not carried out.
