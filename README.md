## Repository containing only example scripts.

# learnings:
# About Workflows
1) Workflow is yml file. Come inside of repository level and consist of jobs.
2) Jobs come inside of Workflow and consists of Steps. If we not defined dependencies then all job run parrallel.
3) Steps come inside of Job and consits of github action scripts what we want to run in steps.  Its run sequentially in side Steps.

# About Events
1) Reposiory Events
    1) push : Trigger when someone push
    2) issues : Trigger by variety of events related to issues
    3) pull_request : Trigger by variety of events related to PRs
    4) fork : Trigger when repository get forked
2) Manual Trigger
    1) Via UI : Trigger by Action tab of github
    2) Via an API call : Trigger by Rest APIs of Github
    3) Via different Workflow : Triggered from withing workflow
3) Schedule : By Cronjob

# Actions
1) nodejs actions : actions/checkout@v4 is default action provided by Github for nodejs and actions/setup-node@v4 is default action to setuo node in runner. 
npx create-react-app --template typescript react-app used to create react app inside directory.
2) Events Filter : We are using it to control workflow run so that it will run whenever we make change in specific branch, tags or ignore any folder.
3) Activity types : We are using it to control workflow run so that it will run whenever anthing we change in lifecycle of any events like pull request (reopened, closed or synchronized)

# Context https://docs.github.com/en/actions/learn-github-actions/contexts#about-contexts

1) github
2) env
3) input
4) vars
5) secrets

# Expression

1) Used of operators and functions
    1) General Purpose functio
        1) contains()
        2) endsWith()
        3) toJSON()
        4) fromJSON()  -- used to chenge from string to any datatypes
    2) Status Check functions
        1) success()  -- used after any step or job...return true if last step success
        2) failure()  -- used after any step or job...return true if last step fail and it will run nxt step
        3) always ()  -- used after any step or job...return true if last step fail or success
        4) cancelled() -- used after any step or job...

# Execution
1) It is used as need by this we can run job as per our requirement
like  
jobs:
    job1:
    job2:
    job3:
        need :
            job1:
            job2:
    job4:
        need :
            job1
job3 will run if job1 and job2 will execute first and job4 will run if job1 excuted first