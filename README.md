epr-laps-performance-tests

The template to create a service that runs WDIO tests against an environment.

This framework comprises of both API nad UI tests. Post extracting, open the tests in 2 sepeate Jmeter tabs. 


Test Data: Make sure the test data are set up correctly

API tests requires .csv file to be set up and requires coordination with FSS team for hige data set up for bank details and payment docs 
User registration is not in scope, so register couple of users spanning across CEO, HoF and HOW and use them fdor data set up with FSS

UI tests requires one valid user who can perform all the activities. Register a HoF who is present in FSS tables as well. Set up bank detials and payment documents for the user and perform the UI performance test
Note: UI Performance test needs to run for the whole duration of API test (they need to run in parallel)


JMeter Set up - 
Set up Jmeter in local system 
Ensure chromedriver is working fine and provide the Chromedriver path in the UI tests. 
Provide the Auth token from Audit logs - Login from UI as a user, navigate to LAPS bank page. Open the audit log and navigate to the login token section where the JWT with token and refresh token will be avilable. Copy t he token and add it in Jmeter appending with Bearer (token here after a space)
x-api-key - Can be taken from POrtal CDP. Sign in and click on the user profile, in the next page select hte x-api-key which is valid ofr 24 hours.