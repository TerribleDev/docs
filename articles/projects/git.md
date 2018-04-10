# Git Repositories
 
## What 
The Stoplight Platform is built on top of Git. This means that all your projects are Git repositories and that our platform benefits from all the additonal functionality provided by Git. To access the Git funtionality, you can use Access Tokens to access the Stoplight API, authenticate Prism in a continuous integration enviornment, and access the underlying Git repositories for projects. 

> You can make this part of your Git workflow, add it to scripts, or your CI/CD process

## Who 

If you have write access to a project, you will be able to:
* Pull projects via Git
* Commit to projects via Git
* Push changes to projects via Git

If you have read access to a project, you will be able to:
* Pull your project via Git

## How to Clone Your Stoplight Git Repository 
  
1. Under the Settings section in your Stoplight account, find the “Access Tokens” section. 

![Access Tokens](https://github.com/stoplightio/docs/blob/develop/assets/images/access-tokens.png?raw=true)

2. Create a token to access projects that your Stoplight account has proper permissions for. These permissions match the ones in the Stoplight UI. 

> You can name your token whatever you want. Once you have created the token, copy it, and only store it in a safe location. Once you close the window, you will not see it again.

3. Store your access token as an environmental variable (recommended)

For example, on Mac/Linux:

```
export STOPLIGHT_TOKEN="1234567890"
```

4. You can then `git clone` the repo, replace `{stoplight-username}`, `{username}`, and `{project-name}` with the appropriate information: 

```
git clone https://{stoplight-username}:$STOPLIGHT_TOKEN@git.stoplight.io/{username}/{project-name}.git
```

For example: 

```
git clone https://taylor:$STOPLIGHT_TOKEN@git.stoplight.io/taylor/test-new.git
```

5. If the project is associated with an organization and not a personal project, replace `username` with `organization-name` 

6. Now you can make changes to your files, commit, and push to your master branch. You can see these changes in the Stoplight UI as well as the "History of Changes" 

> Remember: You will only see changes on the master branch in the UI at this time. 

    
---
**Related Articles**
- [Change a Project Member's Role](/platform/projects/change-a-members-role)
- [Make Your Project Private/Public](/platform/projects/visibility)
- [Invite People to Organization](/platform/organizations/invite-people)
- [Add People to a Team](/platform/organizations/teams/add-people)