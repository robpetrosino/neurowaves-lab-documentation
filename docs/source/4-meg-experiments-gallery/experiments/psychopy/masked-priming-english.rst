.. _maskedpriming:

Experiment example (PsychoPy): Masked Priming English
-----------------------------------------------------

Authors: Crystal Jemy, Roberto Petrosino

Description
^^^^^^^^^^^

A typical masked priming experiment consists of four main parts: 

A. Introduction screen: explanation of the task (lexical decision)
B. Practice: short practice so to ensure the participant familiarizes with the task (usually 10-20 trials)
C. Experiment: actual experiment
D. Break screen: break from the experiment every n number of trials

With respect to (2) and (3), the trials being presented consists of three different kinds of stimuli: 

1. MASK: series of hashes, typically presented for 500 ms. (NB: This will not be coded in the stim files, but directly in the script, since it does not change across conditions)
2. PRIME WORD: a lower-case word, typically presented for a duration between 33 and 50 ms. This may change from experiment to experiment, and will need to be settable at the beginning of each run. 
3. TARGET WORD: an upper-case word, typically presented right after the prime word, for a duration between 2000 and 3000 ms. 

The participant will be asked to decide whether the target word is an existing word in their language by pressing two buttons on the response box. Participants will need to be given the chance to take 4-8 breaks during the experiment. The number of breaks will depend on the total number of trials, so the experimenter will need to be able to set it at the beginning of each run. 

Prime and target words, as well as other variables such as condition(s), correct response, trigger codes, etc. will be included in csv files. An experiment typically consists of two or more different wordlists, so to ensure counter-balancing across participants. The choice of the wordlists should be manually settable at the beginning of each run of the experiment, to so guarantee maximum flexibility to the experimenter. 

TRIGGER CODES. 
The number of trigger codes required varies on the specific experimental design used for each experiment. 

In general, we will need to have:

(i) one code for the mask and the prime
(ii) another code for the target. 

If possible, the target trigger code may vary on the condition being tested. Crystal's experiment consists of 4 word conditions + 1 non-word condition, so it does allow the maximum number of codes (8).

Roberto's experiment adopts a different design and consists of 7*2=14 conditions, so we may just have to use the same code for all targets (regardless of the condition), and then align the MEG clock with the stim log data to match the missing information. 

Finally, we will also want to implement the use of a photodiode, to ensure reliable record of the actual presentation of all stimuli.  


Code Access
^^^^^^^^^^^

:github-file:`Attention task launch experiment <experiments/psychopy/masked-priming-english/meg_attention_task.m>`

:github-file:`Attention task project directory <experiments/psychopy/masked-priming-english/>`


