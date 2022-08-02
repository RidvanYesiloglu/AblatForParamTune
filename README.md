# AblationTrainer
The input taking screen looks like the first image and allows a set of space separated values for each question. After typing parameter sets, it submits the jobs. The results are saved in our group scratch on four folders (detailed_results, job_files, runset_summaries, waiting_jobs). A live summary of the run sets are continously updated and allows to view resulting objective values of all the runs together (see image 2). The detailed results of individual runs (log files, images, or what you specify in write_actions) are saved in detailed_results. Also, the error files and waiting jobs are written. You can use Sherlock's ondemand web interface for looking at these results.

To use it, you need to modify according to your project some lines on<br />
•	the parameters dictionary (params_dictionary) (see image 3. it has kind of a syntax and allows you to specify the sets of parameters. it has a bunch of features (which i do want to bother you with telling) for input validating, specifiying parameter's default, conditionally requiring some of parameters, putting conditions etc.)<br />
•	job script creator python file (runset_train/submit_job_files_given_opts.py)  (this contains job script creation. you may want to request certain amount of resources, load some more modules, change job time, type your email address etc.)<br />
•	of course the models folder (model_xxx.py specifies the model arch., write_actions_xxx.py specifies what to write to logs or what to save in detailed results, plot_xxx.py file is optional and specifies what to plot)<br />

![Image 1: The input taking screen](https://github.com/RidvanYesiloglu/AblationTrainer/blob/main/example_inp_take_screen.png?raw=true)
<p align="center">
    Image 1: The input taking screen
</p>

![Image 2: An example live summary of results of a set of trainings (16 trainings)](https://github.com/RidvanYesiloglu/AblationTrainer/blob/main/example_live_summary.png?raw=true)
<p align="center">
    Image 2: An example live summary of results of a set of trainings (16 trainings)
</p>

![Image 3: An example of the parameters dictionary](https://github.com/RidvanYesiloglu/AblationTrainer/blob/main/example_param_dict.png?raw=true)

<p align="center">
    Image 3: An example of the parameters dictionary
</p>
