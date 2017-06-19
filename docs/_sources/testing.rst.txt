#######
Testing
#######

The SoP Support Service is set up for simple system testing by DVA staff without the requirement to install any software.  This tests the whole system end-to-end, including the server insfrastructure.

Each test case consists consist of a file with the body of the JSON request.  If the file name starts with 'PASS', the SoP Support Service is expected to return at least one SoP factor satisfied.  If the file name starts with 'FAIL', the SoP Support Service is supposed to return no factors satisfied.

The steps to add a new system test are:

1. Ensure you have a GitHub account and have cloned the dva-sop-api-system-tests repository.
2. Upload test files to the folder at https://github.com/govlawtech/dva-sop-api-system-tests/tree/master/src/test/resources/dvaDefinedTestData.

In order to report on these tests cleanly, the results for these tests are collected into a separate web page. 

When a test fails, there are three possible reasons:

#. The format of the test case does not match the expected format.  The error message of the test case may indicate the problem.  The solution is to fix the format of the test case.
#. The expected outcome of the test case does not match the expected outcome for that scenario in the specifications or configuration.  If the expected outcome is correct, the configuration or specifications need to be changed.  If the expected outcome is incorrect, change the expected outcome.
#. The code does not correctly implement the specifications or apply the configuration.  The tracing info in the test case report may indicate the problem.  The solution is to fix the code. 

