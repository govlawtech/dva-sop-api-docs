#############################
AI-assisted Condition Mapping
#############################

This service helps maximise the number of times MyService can automatically
match the veteran's particular condition to one on the list of *SoP* conditions for which DVA provides treatment and compensation.  It uses machine-learning techniques to match the veteran's description of their diagnosis to a SoP condition - as well as conventional text-matching and spell-checking.  The AI component exploits a Microsoft cloud-based commercial natural language processing API: *Language Understanding Intelligence Service* DVA staff claims assessors contributed expert guidance to its initial training. 

The department has historically taken an entirely manual approach to classifying a condition: veterans write their medical condition in free form text on a form. This was either on a paper claim form or an online form called the *Single Online Claim Form*, or more-recently a drop-down box in MyService.

Claims assessment officers then attempt to match the veteran's description to a recognised SoP condition, following policy guidance (Policy Guidance Note AN08, Full Federal Court Decision	- Benjamin v The Repatriation Commission). This can involve time-consuming and frustrating correspondence with the applicant to clarify their condition: their description or their doctor's description rarely matches one of the white-listed SoP conditions closely.  The automatic approach removes this pain in a substantial portion of cases.

Additionally, it makes the most of Decision Ready Processing: it enables MyService to route more claims down the fast-tracked path automatically. Otherwise, these claims would miss out on the fast-tracked processing.

Before using this function, MyService automatically classified only 10.5% of claims into one of the fast-tracked categories: Straight-Through, Streamlined or Computer-Based Decisions. (Source: production logs for MyService from late December 2017 to end of June 2018 showed 6421 claims, of which only 671 were tagged for fast-tracked processing.)

.. figure:: aiMatcher.png
    :scale: 50 %

    Classification of conditions, derived from AI condition matcher logs from week commencing 20 August 2018.  Note that *calls* refers to API service calls - a proxy for claim proportions, but not absolute numbers.

In light of data collected from production, Gov Law Tech and DVA further tuned the AI.  These changes took effect on 1 December 2018.  This increased its effectiveness by 10 to 15% so MyService correctly fast-tracks around half of initial liability claims.