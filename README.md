# PSY2150-Skills-Workshop-1
This is a simple and short memory experiment called a same/different task. 
On each trial, you'll see an object (a green figure called a Greeble), then you'll see a scrambled picture, 
then you'll see a second object. Your job is to decide whether the first object and the second object 
are the same or different!
The whole experiment only lasts a minute or so, and each trial is very fast paced, so be ready!
Your performance on the task doesn't matter at all. 
You can run it multiple times. You can enter wrong answers on purpose. 
You can see what happens if you do something unexpected.
Once you finish each "session" (which is 16 trials), a file will be downloaded to your computer, 
to your Downloads folder. That is your "session log". It will have a record of the presented items, 
and your key press responses. This file is called a CSV (for comma separated values), and it is a common way of formatting data, 
because it is very simple. You can open the CSV file in Excel, or Google Sheets, or even a text editor.

The experiment has two conditions: One is "noise", where visual static is added to the object. The other is 
"no noise" where the objects are presented in the clear, without static.

CLICK HERE TO RUN THE EXPERIMENT FOR YOURSELF: https://jasonkchow.github.io/PSY2150-Skills-Workshop-1/experiment.html
It will start you off with some brief instructions about what keys to press.
Then you can come back here to see some other details about the experiment, below.

Note that this experiment has some intentionally rough edges! 
Part of the group assignment is to give us "notes" on how the experiment could be improved.

## Trial structure

* Present fixation cross (you should fixate your eyes on this)
* Present first image (the "study item")
* Present visual mask
* Present second image (the "probe") until keypress is made

## Materials and procedure

There are four objects (figures called Greebles) in the item pool. On each trial, one of these is chosen pseudorandomly to be presented. 
On "same" trials, the same picture is presented as the study item and the probe. On "different" trials, different pictures are randomly selected as the study item and the probe.
Each object is used once in a "same" trial for each condition. There are 16 trials total. 

Default experiment parameters:
* Fixation time: 500ms
* First image time: 200ms
* Mask time: 500ms
* Intertrial interval: 500ms
* Same key: f
* Different key: j

Default parameters are defined near the top of the experiment file. Changing their values will change the experiment. However, this will not change the experiment hosted at the link above. Jason would have to update it after making changes to those parameters, to have them take effect. 

If additional images are added to the stimuli folder, the experiment code will use them to make more trials. 

The experiment is created using jsPsych (https://www.jspsych.org/).

## Data dictionary

The data csv file has the following columns:
* rt: response time
* response: which key did participant hit (default: f = same, j = different)
* test_trial: a flag for the test trials, for internal filtering
* stimulus1: the first image
* stimulus2: the second image
* same: are the two images the same?
* noise: is there noise overlaid on the images?
* corr_res: the correct response
* time_elapsed: how long has the experiment been going in ms
* sbj_id: randomly generated subject_id
* start_time: date/time that the experiment started
* correct: was the response correct
* seed: random seed used for randomization
