##########################
Decision Ready Processing
##########################

The API applies *Decision Ready Processing* rules, including *Straight-Through*, *Streamlined* and *Computer Based* rules.  These are DVA's innovative policies designed to fast-track claims for certain conditions, based on the veteran's service history.   It applies the rules instantaneously to medical and service history data, and makes a recommendation, justified against current, authoritative primary legal sources. Ultimately, MyService may automatically approve a claim based on this recommendation, or forward it to a delegate with the recommendation attached. 

It has proven scalable and reliable: it has grown from initially three conditions to, at time of writing, these cover 40 conditions, accounting for approximately 77\% of initial liability claims.  MyService typically calls this service several dozen times each day.

Configuration of processing rules is in accordance with rules approved by the Repatriation Commissions and  Military Rehabilitation and Compensation Commission.

Particular rules to note are below.

Mental Health Conditions
************************

For the following conditions, only 'warlike' service counts for automated initial liability recommedations:

* "posttraumatic stress disorder",
* "anxiety disorder",
* "adjustment disorder"

'Warlike' service is as defined in the relevant statutory instruments.
This applies for both MRCA and VEA determinations.

Types of Service
****************

* Currently, 'continuous full time service' counts towards automated initial liability recommendations.  Reserve or cadet service does not count.

Veterans with Multiple Branches of Service
******************************************

* Where a veteran has a service history including multiple service branches (eg, Army and RAN), the standard of proof (Reasonable Hypothesis or Balance of Probabilities) is determined taking into account:
    - the entire service history, including multiple branches;
    - the rank they held in the last service branch in which they started before the condition started.

* Initial Liability recommendations for veterans with service history from multiple branches is are according to the branch which is most beneficial to the veteran.  

Dates and Times
***************

* The number of days of operational service in a given interval is the number of whole elapsed 24 hour periods, rounded up to the nearest day.  This takes account of time zones, daylight saving and leap seconds etc.


* Dates of operations in Service Declarations are assumed to be in the "Australia/ACT" IANA TZDB time zone.  The start time is assumed to be 12 AM on the date specified in the Declaration.  End dates of operations are assumed to be inclusive: the end time is assumed to be 12 midnight PM on the date specified.

* Commencement dates and dates of effect are assumed to be in the "Australia/ACT" IANA TZDB time zone, at 12AM.
