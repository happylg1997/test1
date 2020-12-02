RUN
===

1.Requirements:<br>
  * python3, tensorflow2.1<br> 
  
2.data:<br>
  * You need to concat the input-image and ground-truth together. The left is ground-truth and the right is input-image,just like the datasets I provided.<br>
  
3.Steps to run:<br>
  * Go to the root directory and run: <br>
   `python create.py -n app_name`<br>
    where `app_name` is the name of the project you want to create.Now the project that needs training has been created in the `./app/app_name` directory.<br>
  * Enter the `./app/app_name` directory and modify `config.json` which is configuration file<br>
    * data_dir  :   The storage location of the data set, the default is the data folder in the root directory.
    If you need to train on other datasets, please modify this configuration<br>
    * training_device : Decide which graphics card to use. If you want to specify a graphics card for training，just modify the value as `GPU:0-only`, 
    it means use GPU:0 for training.
    * callback_args : It is used for loading watermark. `--wm_path--` is the path of watermark.  `--wm_width` is the shape of watermark.
    * lambda  : It is the weight of loss(2) and loss(3)
  * Run `train.sh` (for linux) to start training.
  
  So if you want to strat training  ,   just three steps:
  * Go to the root directory and run `python create.py -n app_name`. 
  * Enter the `./app/app_name` directory and modify the `training_device` to specify a graphics card for training.
  * Enter the `./app/app_name` directory and run `train.sh` (for linux) to start training.
  * If you want to run this code in windows , please modify all paths in code and configuration file.
 
