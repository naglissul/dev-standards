# dev-standards  
Here I will be listing the standards I use for software development  
- Versioning (semantic versioning)
- Tests and their structure
- Deployment process (pipelines, dockers and stuff like that)
- Project file structure
  
# Versioning
Using GitHub and, of course, git.  

## Changelog
https://keepachangelog.com/en/1.1.0/
## Semantic versioning
https://semver.org/
  
# Project setup (how to start a project)
1. Make a template (template examples will be created in this repository)
2. Make a changelog
3. Have a DESIGN.md file (or use JIRA)
4. ......

# Environments
https://www.flagship.io/test-environment/
https://dev.to/preethamsathyamurthy/git-branching-and-branching-strategy-4mci
https://relevant.software/blog/software-development-process/

- Dev (develop)
- Test (test)
- Stage (staging/syst)
- Prod (master/main/prod/live)

Basically:  
1. create a feature on feature branch.  
2. PR to develop branch.  
3. When all the features are merged to the develop branch, merge (without the PR) from develop -> test is made. 
4. Everything is tested thoroughly on test branch - including the inspecting of code quality. The changes are made here, if needed.
5. test -> staging. Builds are made in test environment and sent to staging environment. In staging - only builds(?). And they are reviewed by product owner or client
6. When everything is reviewed, PR from staging -> master. Here everything is in production and can be seen for users
