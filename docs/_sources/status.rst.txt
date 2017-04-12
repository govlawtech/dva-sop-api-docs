#############
Status
#############


.. |check| unicode:: 10003 .. checkmark
.. |cross| unicode:: U+2717 .. cross

.. list-table:: SoP Coverage
  :widths: 5 5 5 5
  :header-rows: 1
  
  * - SoP
    - Auto-updating factors
    - Wear and Tear Processing
    - Acute Processing
  * - Lumbar Spondylosis
    - |check|
    - |check|
    - |cross|
  * - Osteoarthritis
    - |check|
    - |cross|
    - |cross|
  * - Thoraic Spondylosis
    - |check|
    - |cross|
    - |cross|
  * - Cervical spondylosis
    - |check|
    - |cross|
    - |cross|
  * - Chondromalacia patella
    - |check|
    - |cross|
    - |cross|
  * - Epicondylitis
    - |check|
    - |cross|
    - |cross|
  * - Haemorrhoids
    - |check|
    - |cross|
    - |cross|
  * - Iliotibial Band Syndrome
    - |check|
    - |cross|
    - |cross|
  * - Inguinal hernia
    - |check|
    - |cross|
    - |cross|
  * - Internal derangement of the knee
    - |check|
    - |cross|
    - |cross|
  * - Irritable bowel syndrome
    - |check|
    - |cross|
    - |cross|
  * - Joint Instability
    - |check|
    - |cross|
    - |cross|
  * - Posttraumatic stress disorder
    - |check|
    - |cross|
    - |cross|
  * - Sleep apnoea
    - |check|
    - |cross|
    - |cross|
  * - Pes planus
    - |check|
    - |cross|
    - |cross|


.. list-table:: SoP Reference Service - Service Determinations
   :widths: 15 10 30
   :header-rows: 1

   * - Requirement
     - Specs Ref
     - Status
   * - Get Operations query - API endpoint, error msgs, validation
     - 4.2
     - |check| [#f16]_
   * - Download Service Determinations from Legislation Register
     - 4.2
     - |check|
   * - Extract operation dates and names from tables on Legislation Register
     - 4.2
     - |check|
   * - Convert operations to JSON and store/retrieve
     - 4.2
     - |check|
   * - Order operations by start date
     - 4.2
     - |check|
   * - Handle operations without end date
     - 4.2
     - |check|
   * - Handle operations without title
     - 4.2
     - |check|
   * - Declared operations update automatically
     - 4.2
     - |cross|
     

.. list-table:: SoP Reference Service - SoPs
   :widths: 15 10 30
   :header-rows: 1

   * - Requirement
     - Specs Ref
     - Status
   * - Get SoP factors query - validate input and error messages
     - 4.2
     - |check|
   * - Retrieve authorised PDFs from Legislation Register
     - 4.2
     - |check|
   * - Convert authorised SoP PDF to plain text
     - 4.2
     - |check|
   * - Cleanse SoP plain text to remove footnotes, compress spaces etc.
     - 4.2
     - |check|
   * - Extract register ID from SoP text
     - 4.2
     - |check|
   * - Extract instrument number from SoP text
     - 4.2
     - |check|
   * - Extract factors from SoP text
     - 4.2
     - |check|
   * - Extract definitions from SoP text
     - 4.2
     - |check|
   * - Link definitions to factor text
     - 4.2
     - |check|     
   * - Extract ICD codes from SoP text
     - 4.2
     - |check|
   * - Storage and retrieval of SoPs from database
     - 4.2
     - |check|
   * - Handle dates without time zone info
     - 4.2
     - |check|
   * - New SoPs are automatically detected
     - 4.2
     - |check|
   * - New SoP compilations are detected
     - 4.2 
     - |check|
   * - Revoked SoPs are removed
     - 4.2
     - |check|
   * - SoPs revoked and replaced are swapped
     - 4.2
     - |check|
   * - Batch job to run updates nightly
     - 4.2
     - (almost!)
     

    
.. list-table:: SoP Support Service
   :widths: 15 10 30
   :header-rows: 1

   * - Requirement
     - Specs Ref
     - Status
   * - Handles expected inputs
     - 4.1.1
     - |check| (also includes rank)
   * - Count days of operational service
     - 4.1.2
     - |check|
   * - Determine whether RH or BoP SoP applies
     - 4.1.2
     - |check|
   * - Determine satisfied factors
     - 4.1.2
     - |check|
   * - Handle service in multiple service branches
     - 4.1.2
     - |check|
   * - Logic to determine satisfied SoP factors
     - 4.1.2
     - |check|
   * - Logic to determine progress towards threshold
     - 4.1.2
     - |cross|
   * - Acute conditions - exact date
     - 4.1.2
     - |cross|
   * - Acute conditions - date range
     - 4.1.2
     - |cross|
   * - Logic for wear and tear with exact date or date range
     - 4.1.2
     - |check| 
   * - Logic for wear and tear for aggravation/worsening
     - 4.1.2
     - (would need further specs)
   * - Machine-readable output
     - 4.1.3.1
     - |check|
   * - Human-readable output
     - 4.1.3.2
     - (still needs pie chart and API endpoint)





.. list-table:: Technical Requirements
   :widths: 15 10 30
   :header-rows: 1
   
   * - Requirement
     - Specs Ref
     - Satsified?
   * - Platform: Java Standard Edition 8
     - 4.3.1
     - |check| [#f1]_
   * - Application Server: Jetty
     - 4.3.2
     - |check| [#f2]_
   * - Form of requests and  responses (JSON,REST,GET only, error codes, date formats)
     - 4.3.3
     - |check| [#f3]_ 
   * - Validates configuration on application start and logs errors               
     - 4.3.4
     - |check| [#f4]_
   * - Configurable Throttling based on the number of requests from an IP address 
     - 4.3.4(b)
     - |check| [#f5]_ 
   * - Security - secured aganist JSON and REGEX DOS attacks
     - 4.3.5(a)
     - |check| [#f6]_
   * - Security - Securured against CSRF attacks
     - 4.3.5(b)
     - |check| [#f7]_
   * - Security - configured for TLS 1.2 exclusively
     - 4.3.5(c)
     - |check| [#f8]_ 
   * - Security - validates incoming Content-Types and Response-Types
     - 4.3.5(d)
     - |check| [#f9]_ 
   * - Security - responses include header: X-Content-Type-Options: nosniff.
     - 4.3.5(e)
     - |check| [#f10]_
   * - Server Configuration - CORS enabled
     - 4.3.6(a)
     - |check| [#f11]_ 
   * - Server Configuration - Gzip compression enabled
     - 4.3.6(b)
     - |check| [#f12]_
   * - Code Quality Metric: FindBugs 2.0
     - 4.3.7
     - |check| (substantially) [#f13]_
   * - Performance: average TTFB of less than 500ms
     - 4.3.8
     - |check| [#f14]_
   * - Deployment: UNCLASSIFIED (DLM) certified cloud PaaS
     - 4.3.9
     - |check| [#f15]_


.. list-table:: Bonuses
   :widths: 15 10 30
   :header-rows: 1

   * - Bonus!
     - Benefit
     - Status
   * - Java client
     - Easier for DVA to use API
     - |check|
   * - Plain text configuration of rules
     - Easier for DVA to change rules
     - idea

.. rubric:: Notes

.. [#f1] Java version "1.8.0_111" Java(TM)<br>SE Runtime Environment (build 1.8.0_111-b14)<br>Java HotSpot(TM) 64-Bit Server VM (build 25.111-b14, mixed mode)
.. [#f2] Runs on Jetty Distribution 9.3.14.

.. [#f3] Note one exception: the HTTP request to the SoP Support Service to determine satisfied factors according is a POST rather than a GET.  This is for better compatibility with security testing tools.
 Java's OffsetDateTime class with standard formatters for ISO date times.  Date strings ending in 'Z' with no time information are assumed to be 12am midnight UTC. (eg '2017-01-01Z')

.. [#f4] Logging throughout application using SL4J.

.. [#f5] Configurable but not configured. To configure, add the Jetty Denial of Service filter as described here: http://www.eclipse.org/jetty/documentation/current/dos-filter.html.

.. [#f6] Parsing of API routes primarily uses Java's equality operator, not REGEX: see https://github.com/perwendel/spark/blob/master/src/main/java/spark/route/RouteEntry.java.  A regex is used for matching query parameters, however it does not have any groups with repetition: see https://github.com/perwendel/spark/blob/master/src/main/java/spark/QueryParamsMap.java.

          The API uses the Jackson library to parse JSON in requests.  By default, this includes protection against JSON DOS attacks: see FAIL_ON_SYMBOL_HASH_OVERFLOW(true) in https://github.com/FasterXML/jackson-core/blob/master/src/main/java/com/fasterxml/jackson/core/JsonFactory.java

.. [#f7] The API is secured against this by design as it is stateless.
.. [#f8] Jetty uses this configuration by default: see http://www.eclipse.org/jetty/documentation/current/configuring-ssl.html

.. [#f9] The API returns HTTP status code 406 if Content-Type is not 'application/json'.  See: https://raw.githubusercontent.com/govlawtech/dva-sop-api/devtest/src/main/java/au/gov/dva/sopapi/Application.java

.. [#f10] See: https://raw.githubusercontent.com/govlawtech/dva-sop-api/devtest/src/main/java/au/gov/dva/sopapi/Application.java.

.. [#f11] Enabled via Windows Azure management portal.  Could also be enabled via web.xml: see http://www.eclipse.org/jetty/documentation/current/cross-origin-filter.html.

.. [#f12] Jetty applies Gzip compression for all GET methods by default: see /etc/jetty-gzip.xml.


.. [#f13] FindBugs runs on the devtest branch continuously via Travis CI.  This is configured in the build.gradle file.  It fails the build if any bugs are found.  FindBugs is set to the maximum level of scrupulousness.  So if the build is passing, it means FindBugs has found no bugs.  This applies to all FindBugs categories, not just Security and Malicious code vulnerability.  FindBugs is excluded from running on Scala code because it is not designed for Scala code and throws too many false negatives.  The Scala code is concerned with parsing SoPs.

.. [#f14] Adhoc tests show TTFB of less than 150ms.

.. [#f15] Deployed to Microsoft Azure, Sydney or Melbourne data center.  Details of ASD compliance are at https://www.microsoft.com/en-us/TrustCenter/Compliance/CCSL under 'letters of compliance and certification'.

.. [#f16] The Get Operations query does not take a query date as on reflection in didn't add any functionality and just added complexity.  The query simply returns the latest declared operations at the time of the query.


