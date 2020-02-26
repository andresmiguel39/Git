# Commads in a project

## How it sould be

Update into repository and deploy. 

1. Go into repository
```shell
  cd C:/Repository_XXXX10/XXXX10001_Name_APP
```
2. Do a checkout, it allows you to set over the branch 
```shell
  git checkout master <brachname> #(develop - release - master)
```
3. We can use *-D* in case of you need to delete a branch and it deletes also on VSTS or any repository 
```shell  
  git branch -D <brachname>
```  
4. Update local repo
```shell
  git pull origin
```  
5. Create new branches
```shell
  git checkout -b features/HA_XXXXX203  
```
5. Copy files from outside or add new files to our local repo
```shell
  cp /path/from/copy .
```
6. Must be on red with the followed command
```shell
  git status
```
7. To add all the files to the branch
```shell
   git add -A 
```
8. Now everything must be on green
```shell
  git status
```
9. Commit changes
```shell
  git commit -m "installation package HA_XXXXX203"
```
10. Push up all the changes to a repository
```shell
  git push origin <nombre de rama (featuresfeatures/HA_XXXXX203-06145)
```
11. If you are not familiar with Git remote repos, it is better to check it in that repository  

12. Then we need to go to _pull requests_ and create one, then select the branch (depends of the environment), and then select also the work item for example de SU for isntalation and then create it, then, we need to wait to code review en and an aprpoval to make the merge.

13. After that go to pipelines en verify the status of CI, it must brind the new changes and compare en CD in the artifactory and it does a diff between files. 

14. Go to pipelines of releases en verify the deployment.

15. If it fails, you can try redeploying again.
