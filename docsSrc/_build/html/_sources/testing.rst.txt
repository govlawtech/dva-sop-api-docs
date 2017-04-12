#######
Testing
#######

The SoP Support Service is set up for simple system testing by DVA staff without the requirement to install any software.  This tests the whole system end-to-end, including the server instrastructure.

Each test case consists consist of a file with the body of the JSON request.  If the file name starts with 'PASS', the SoP Support Service is expected to return at least one SoP factor satisfied.  If the file name starts with 'FAIL', the SoP Support Service is supposed to return no factors satisfied.

The steps to add a new system test are:

1. Ensure you have a GitHub account and have cloned the dva-sop-api repository.  The Digital Transformation Agency runs courses on Git and GitHub, and there is also ample documentation online. 
2. Upload test files to the folder at https://github.com/govlawtech/dva-sop-api/tree/dvatesting/client/src/test/resources/dvaDefinedTestData
3. Submit a pull request via GitHub. 
4. When the repository owner accepts your pull request, the tests will run automatically.  The 'Build Status' icon at https://github.com/govlawtech/dva-sop-api shows whether there are any failures.  If you click the icon, it will show the log of the test run.  This *may* indicate the reason for any failures.

 


