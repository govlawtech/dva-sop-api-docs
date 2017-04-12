##############
Specifications
##############

`Specification Document <resources/specs.pdf>`_

`SoP list <resources/sops.csv>`_


****************************
Clarifications
****************************

* For the SoP Support Service, the incident type can be set to 'aggravation'.  This is intended to cover injuries or diseases covered by Section 27(d) and 30 of MRCA: basically non-service conditions made worse by service [#f1]_.  If the incident type is 'aggravation', the user of the service needs to provide both an onset date (or range of dates) and an aggravation date (or range of dates).  The requirement for both dates is to help evaluate SoP factors where the time between initial onset and aggravation is important.

******************************
Variations from Spec
******************************

* The array label for the array of legislative instrument ID's in the example response to the Get Operations query is ```registerIDs``` rather than ```legislativeInstrumentIds```, to be consistent with the terminology on Legislation.gov.au and elsewhere.

* The label shown as ```registeredId``` in the example response for the Get Sop Factors query is actually ```registerId```.


.. rubric:: Footnotes

.. [#f1] See discussion in  *Larter and Military Rehabilitation and Compensation Commission (Compensation) [2017] AATA 67 (25 January 2017) for discussion)* (http://www.austlii.edu.au/au/cases/cth/AATA/2017/67.html).
