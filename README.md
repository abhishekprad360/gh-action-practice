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