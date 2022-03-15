# SpriteCloudApi

#Reqirements
- Java v.15
- maven
- Jenkins
- Postman

Repo Link: https://github.com/HudaKhaled/SpriteCloudApi

# How to run tests manually

1. Get clone from the repo using git clone command: git clone git@github.com:HudaKhaled/SpriteCloudApi.git

2. Go to the repo on your local machine and check out master using this command: git checkout master

3. Open the collection along with the environment variables in postman

4. Select the collection and run

## To run from cmd using newman:

 1. Go to project directory, install newman using >> npm install -g newman
 
 3. Write this command to run the collection along with the enviroment variables: 
 newman run SpriteCloudApi.postman_collection.json -e SpriteCloud.postman_environment.json
 
 4. To excute a new xml report, use this command and check the directory to see the generated report:
 newman run --reporters junit SpriteCloudApi.postman_collection.json -e SpriteCloud.postman_environment.json


# How to run tests from CI - Jenkins
1. In the directory where "jenkins.war" is downloaded, run this command "java -jar jenkins.war" to run jenkins

2. Open http://6d4c-45-247-92-207.ngrok.io/job/SpriteCloudApi/ to check the configured job

3. Run these 3 commands
 - Create new branch, empty commit, to make a pull request to trigger the build on jenkins

    1. git checkout -b Noref-trigger-tests-version-60

    2. git commit --allow-empty -m "trigger tests"

    3. git push -u origin Noref-trigger-tests-version-60

4. Then go to the repo on git, make pull request, and merge

5. Check the triggered build on http://6d4c-45-247-92-207.ngrok.io/job/SpriteCloudApi/
