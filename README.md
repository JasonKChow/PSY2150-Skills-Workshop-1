# PSY2150-Skills-Workshop-1
This is a simple same/different experiment where participants need to decide 
whether a pair of objects are the same or different. There are two conditions:
noise and no noise. In the noise condition, the objects are presented with 
uniformly distributed noise overlaid. In the no noise condition, the objects
are presented normally. After the experiment is finished, the relevant data is
downloaded as a csv.

On each trial, it starts with a fixation cross, followed by the first image,
after a short exposure time, a visual mask is displayed, and then finally the
second image is presented. The second image stays on the screen until a 
response is made.

The experiment is hosted here: https://jasonkchow.github.io/PSY2150-Skills-Workshop-1/experiment.html

## Default experiment setup
There are four objects that are pseudorandomly selected to create trials. Each
object is used once in a "same" trial for each condition. The "different" 
trials are created by randomly selecting two different objects. This results in 
a total of 16 trials. 

Default experiment parameters:
* Fixation time: 500ms
* First image time: 200ms
* Mask time: 500ms
* Intertrial interval: 500ms
* Same key: f
* Different key: j

Default parameters can be changed near the top of the experiment file. 
Additional images can be added and will follow the same rules for generating
trials.

The experiment is created using jsPsych.

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
