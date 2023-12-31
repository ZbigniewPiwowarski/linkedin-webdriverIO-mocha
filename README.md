# linkedin webpage functional tests
- tests for anonymous not logged in user
- test run on production: https:/linkedin.com

# technologies used
- typescript
- webdriverIO
- mocha
- docker

# test principles
- tests run in headless mode
- every test is independent from each other
- every test runs on browser with clean cache
- tests attempt to be rather general to avoid maintaining costs 
    but to provide some level of safety for general features
    for not logged in user
- after test fails there will be screenshot in main folder with moment when there was a fail


# requirements
- docker https://docs.docker.com/get-docker/

# how to run tests
- once you have installed docker type in root directory: 
docker build -t mytest -f .dockerfile .
# mac
- after docker image was built for running tests type:
docker run -v $PWD:/app -it mytest npm run wdio
# windows
docker run -v %cd%:/app -it mytest npm run wdio

# screenshots
- tests run in headless mode, above command will add screenshots from failed tests to the root directory of repository as well as run tests
- names of the screenshots correspond to the name of error


