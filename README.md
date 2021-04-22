# NETS213-FinalReadMe for Final Project - Part 2

Major Components:

Aggregate List of Keywords: In the first part of the project we will be creating a list of possible keywords to be the general topic of the Sonnet. Some examples of these keywords could include food, love, Philadelphia, etc. We will manually choose around 15 keywords. 

Milestones:
- Create the list of words by meeting together and choosing the best topics we see fit

HIIT 1: Rank keywords to determine the Sonnet topic: We will then create the first HIIT, where people will rank the sonnet topics. This will be sent out to around 20 people. This will allow us to crowdsource the ranks for the topics to be able to choose the best possible topic for our Sonnet. We will use the best-ranked topic for our Sonnet. 

Milestones:
- Create the HIIT instructions, design, and price per HIIT
- Submit the HIIT onto Mechanical Turk
- Aggregate the results and choose the HIIT with the best score

HIIT 2: Create a 4 Line Stanza Following an Alternating Rhyme Scheme: We will then create the second HIIT, where people will create a 4 line stanza following an alternating rhyme scheme around the topic chosen in HIIT 1 where every line has to have 10 syllables. This HIIT will be completed by around 50 people. We will then aggregate the results from the 50 workers, and so we will have 50 distinct 4 line stanzas surrounding the topic from HIIT 1.

Milestones:
- Create the HIIT instructions, design, and price per HIIT
- Submit the HIIT onto Mechanical Turk
- Aggregate the results of the HIIT

Quality Control: Use Python Code to Count Syllables, Check for Duplicate Lines, and Check for Correct Rhyme Scheme: We will then run the aggregated results through 3 pieces of Python code. The first will analyze all the HIIT’s and count the syllables in each line to make sure it follows the requirement of 10 syllables per line for a Sonnet. We will then run the HIIT 2 results through another piece of code that checks for duplicate lines, as well as another piece of code that checks for the correct rhyme scheme. We will discard the HIITs that do not pass all three requirements. We will then aggregate the HIIT results that pass all 3 requirements. 

Milestones:
- Create code for Quality Control that counts syllables, checks for duplicate lines, and checks for correct rhyme scheme
- Run the code on the aggregated HIIT 2 results
- Aggregate the HIIT 2 results that pass all 3 quality control tests

HIIT 3: Crowd Votes on Stanzas Based on Content and Relevance to Keywords: We will then create our third HIIT, where the crowd will vote on the stanzas that passed the QC tests. The crowd will be given instructions to choose the best stanza based on the content and relevance to the specific keyword. This HIIT will be completed by around 50 people. Aggregate the results from the 50 workers. 

Milestones:
- Create the HIIT instructions, design, and price per HIIT
- Submit the HIIT onto Mechanical Turk
- Aggregate the results of the HIIT

Aggregation: The Winning 4 Lines are Appended to the Poem and the Process is Repeated: We will then aggregate the results from the 3rd HIIT, and choose the stanza with the highest number of votes. This stanza will be appended to our sonnet. We will then repeat steps 3-6 three times to build a preliminary sonnet 12 lines long. 

Milestones:
- Aggregate results from previous HIIT and choose stanza with highest votes
- Append stanza to sonnet
- Repeat steps 3-6

HIIT 4: Create a 2 Line Couplet to Best Conclude the Sonnet: We will create our 4th HIIT where the workers will be presented with the 10 line preliminary sonnet and their job is to create two lines that best conclude the sonnet, keeping into account the rhyming and syllables requirements. This HIIT will also be completed by around 50 workers. Aggregate the results from the 50 workers. 

Milestones:
- Create the HIIT instructions, design, and price per HIIT
- Make sure the HIIT includes the preliminary 10 line sonnet that we created
- Submit the HIIT onto Mechanical Turk
- Aggregate the results of the HIIT

Quality Control: Use Python Code to Count Syllables, Check for Duplicate Lines, and Check for Correct Rhyme Scheme: We will then run the aggregated results through 3 pieces of Python code. The first will analyze all the HIIT’s and count the syllables in each line to make sure it follows the requirement of 10 syllables per line for a Sonnet. We will then run the HIIT 2 results through another piece of code that checks for duplicate lines, as well as another piece of code that checks for the correct rhyme scheme. We will discard the HIITs that do not pass all three requirements. We will then aggregate the HIIT results that pass all 3 requirements. 

Milestones:
- Use code for Quality Control that counts syllables, checks for duplicate lines, and checks for correct rhyme scheme from step 4
- Run the code on the aggregated HIIT 4 results
- Aggregate the HIIT 4 results that pass all 3 quality control tests

HIIT 5: Crowd Votes on Best Couplet Based on Content, Cohesion, and Relevance to Keywords: We will then create our fifth HIIT, where the crowd will vote on the best couplet that passed the QC tests. The crowd will be given instructions to choose the best couplet based on the content and relevance to the specific keyword. The cohesion of the couplet with the rest of the sonnet should also be taken into account by the workers. This HIIT will be completed by around 50 people. Aggregate the results from the 50 workers. 

Milestones:
- Create the HIIT instructions, design, and price per HIIT
- Submit the HIIT onto Mechanical Turk
Aggregate the results of the HIIT

Aggregation: The Winning Couplet is Appended to the Poem: We will then aggregate the results from the 5th HIIT, and choose the coupley with the highest number of votes. This couplet will be appended to our sonnet. We now have a fully finished sonnet using the power of the crowd!

Milestones:
- Aggregate results from previous HIIT and choose couplet with highest votes
- Append couplet to sonnet


STEP 1: Gather any materials that you need to start 
4/22/2021 
Format of our Project: 

Brief Explanation of Aggregation Process: At each set of HITS, the status of our sonnet changes. At HITS #1 and #2, we input just the keyword, allowing turkers to set the framework for what will become the first quatrain. The most popular quatrain as outputted in HIT #2 is then fed into HIT #3 as how much of the sonnet is currently complete. We continue this iterative process of growing the sonnet until we reach the couplet at which point our sonnet is done. 

Sample QC Inputs and Outputs: 

Our QC algorithm will receive a selection of sonnet stanzas from the workers and it will only move the stanza through if it fits the following criteria: 
Each line has 10 syllables
No duplicate lines and 4 total lines
The stanzas follow an alternating rhyme scheme while the couplet follows a AA rhyme scheme
Sample Inputs:

	Input 1:

	What is the meaning of love
	Love is a complicated thing 
	Love is like a dove
	Love has a great zing
	

	Input 2:

	Love is an essential part of life
	Love is an essential part of life

	Input 3:

	Love oh love why is it needed so much
Oh life would be simple without love’s pains
Love oh love it should not be such a sludge
But I do love thee and I can’t abstain

Output:
	Input 3:

	Love oh love why is it needed so much
Oh life would be simple without love’s pains
Love oh love it should not be such a sludge
But I do love thee and I can’t abstain

Sample Aggregation Module Inputs and Outputs: 

Our aggregation module will work using majority vote, where for all the valid stanzas, workers will vote on them and we will use a majority vote algorithm to get the stanza with the most votes. This stanza will be appended onto our sonnet.
Sample Inputs:

	Input 1:

	(25% votes for Input 1)

	True love takes shape as a strongest fire,
In the mind forever burning away,
Never sick, never dead, never cold or tire,
I stand to the side; my response is to pray 
	

	Input 2:

	(35% votes for Input 1)

	All this pain, still I want her here and now 
My heart aches for her, my heart calls for her 
Lest, she is gone, I’m left wondering how
Memories here that will soon be a blur  

	Input 3:

	(40% votes for Input 3)

	Love oh love why is it needed so much
Oh life would be simple without love’s pains
Love oh love it should not be such a sludge
But I do love thee and I can’t abstain

Output:
	Input 3:

(40% votes for Input 3)

	Love oh love why is it needed so much
Oh life would be simple without love’s pains
Love oh love it should not be such a sludge
But I do love thee and I can’t abstain

Reasoning: Input 3 has the highest vote count so our aggregation module will output input 3 and append it to our sonnet.
 
