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

* Initial Liability recommendations for veterans with service history from multiple branches is according to the branch which is most beneficial to the veteran.  

Dates and Times
***************

* The number of days of operational service in a given interval is the number of whole elapsed 24 hour periods, rounded up to the nearest day.  This takes account of time zones, daylight saving and leap seconds etc.


* Dates of operations in Service Declarations are assumed to be in the "Australia/ACT" IANA TZDB time zone.  The start time is assumed to be 12 AM on the date specified in the Declaration.  End dates of operations are assumed to be inclusive: the end time is assumed to be 12 midnight PM on the date specified.

* Commencement dates and dates of effect are assumed to be in the "Australia/ACT" IANA TZDB time zone, at 12AM.

Counting Days of Service
************************

The policy intention is to count whole days of service.  The issue is how to do this given the service history data.

In particular, the service history data:

* Has local dates: no time zone information;
* Sometimes has sequences of the same operation with the same start and end day;
* Does not indicate explicitly whether the end date is inclusive or exclusive - although the fact that there are operations where the end date of one matches the start date of another suggest it is exclusive.

For the purpose of counting days of service:

* We assume the time zone is IANA time zone 'Australia/Canberra'.  The location of the operation is irrelevant.  The justification for this is that it enables easy comparison with dates in the legislative instruments.  The dates in the legislative instruments are in this time zone.
* We assume that the end date of intervals is actually inclusive.  This is different to normal practice for storing date intervals.  There are two justifications for this.   Firstly, it is most favourable to the applicant.  Secondly, it matched what delegates and testers expected.  It also probably matches what a veteran would expect when entering service history manually.  (This was a deliberate change by DVA from an earlier version where we treated the end dates as exclusive, which was on my mind.)

The consequence of these assumptions is that we need to adjust start and end dates when a service record shows an operation starting and ending on the same day.  These are otherwise 'overlapping': assuming the end date is inclusive.  We subtract one day from end dates which overlap with subsequent operations.  Otherwise there would be double counting.