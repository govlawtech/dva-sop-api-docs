#############################
Automatic SoP Update
#############################

There are four cases where SoP changes are handled automatically:

1. A new SoP instrument, which not not repeal any existing instruments (e.g.: for a previously unrecognised condition).
2. An amendment to an existing SoP instrument.
3. A new SoP instrument which repeals one or more existing instruments.
4. Revocation of an existing SoP without any replacement.

**************************************
New SoP instruments for new conditions
**************************************

For first case, notification of the new SoP comes from the email updates services of the Legislation Register.  An example notification is::

   Amendment Statement of Principles concerning anxiety disorder No. 100 of 2016
   Amendment Statement of Principles concerning anxiety disorder.
   Item was published on 1/11/2016
   https://www.legislation.gov.au/Details/F2016L01698


Following notification, the API retrieves the SoP from the Legislation Register and adds it to its database.

***********************
Amended SoP instruments
***********************

For this case, we wait until the Legislation Register publishes an updated compilation for the instrument.  The API retrieves the latest compilation by polling the Legislation Register (using the '/Latest', see https://www.legislation.gov.au/Content/Linking).
This occurs for all SoPs in the database regularly, at least every 24 hours.  When the Legislation Register indicates the latest compilation has a different Register ID to the one held in the database, the API *replaces* the existing one.

************************************************
New SoP instrument repealing existing instrument
************************************************

For SoP instruments already in its database, the API regularly polls the Legislation Register to check if they have been repealed, ceased or revoked.  When this has happened, the Register gives a pointer to the repealing instrument as well as the date of repeal.  The API retrieves this new instrument and loads it to its database as a replacement SoP.  It end dates the previous SoP.  The end date of the previous SoP is the date *one day before* the date of effect of the new SoP.

********************************
Cease/Repeal without Replacement
********************************

This works similarly to the previous case, except that the repealing instrument is not a SoP in its own right.  If the API cannot identify the repealing instrument as a new SoP (the case above), it end dates the existing SoP in its database.  The end date is the date of repeal shown on the Legislation Register.

