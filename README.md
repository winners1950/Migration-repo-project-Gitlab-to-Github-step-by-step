# Migration from Gitlab to Github

## Introduction

* Owner: Ray Efa
* Activities I like to do: Reading,technology and documentaries

### Step 1: Initialise both Gitlab SCM and Github SCM with an SSH key
   
## Generate an SSH key from your terminal   
ssh-keygen

## Cat the ONLY the public key
cat ~/.ssh/id_ed25519.pub (it maybe a different id-number from your terminal)

### For Gitlab the procedure is below:
 
   Go to settings in the Gitlab account --> Repository --> Deploy Keys (Expand) --> Add new Keys --> Title the Key and
   Paste the key in the box --> Add key to save and quit, (this completes the initialisation of your local environment and 
   the Gitlab account. Remember at work you must need full access for the repository). After all these process, you can now be a
   able to clone from this account in Gitlab

### For Github the procedure is below:

   Go to setting --> SSH & GPG Keys --> New SSH Key --> Title the key, paste the key inside the box --> Add Key to save 
   and quit (this completes the initialisation of your local environment and the Github account.) After all these process is 
   done, you can now clone from this account in Github etc.


## Getting started with Migrating a Gitlab repo to Github.

## Migrating a repository from GitLab to GitHub can be done in a few straightforward steps. Here’s a step-by-step guide to help you through the process:


### Step 1: Prepare Your GitLab Repository
1. *Log in to GitLab*: Access your GitLab account and navigate to the repository you want to migrate.
2. *Clone Your Repository*: Open your terminal (or Git Bash) and clone your GitLab repository to your local machine using the following command:
   
   git clone --mirror https://gitlab.com/username/repository.git
   
   Replace username and repository.git with your GitLab username and the repository name.

### Step 2: Create a New Repository on GitHub
1. *Log in to GitHub*: Go to GitHub and log in to your account.
2. *Create a New Repository*: Click the “+” icon in the top right corner and select “New repository”.
3. *Repository Settings*: Fill in the repository name, description, and choose whether it should be public or private. Do not initialize with a README, .gitignore, or license, as this can cause conflicts later.
4. *Create Repository*: Click on the “Create repository” button.

### Step 3: Push the Cloned Repository to GitHub
1. *Navigate to the Cloned Repository*: Change your directory to the cloned repository:
   
   cd repository.git
   
2. *Add GitHub as a Remote*: Add your newly created GitHub repository as a remote:
   

   git remote add github https://github.com/username/repository.git

   
   Again, replace username and repository.git with your GitHub username and repository name.
   
3. *Push to GitHub*: Push all branches and tags to GitHub:
   

   git push --mirror github
   

### Step 4: Verify the Migration
1. *Check GitHub*: Navigate to your GitHub repository in your browser and verify that all branches, commits, and tags have been migrated successfully.
2. *Check Issues and Pull Requests*: If you want to migrate issues and pull requests, you may need to use a migration tool or script, as they do not automatically transfer in this process.

### Step 5: Update Local Copies (If Necessary)
If you have local copies of the repository that are still pointing to GitLab, you may want to update those to point to GitHub:
1. *Change Remote URL*: For each local clone, you can update the remote URL using the following command:
   bash
   git remote set-url origin https://github.com/username/repository.git
   

### Step 6: Inform Your Team
If you are working in a team, inform everyone about the migration, so they can update their links and ensure they are working with the new GitHub repository.

### Optional Step: Migrate Issues and PRs
- For migrating issues, you can consider using third-party tools like [issues-importer](https://github.com/marketplace/actions/issues-importer) or [githubissues](https://github.com/jenniferbland/github-issues) to help with this process.

That's it! You have successfully migrated your repository from GitLab to GitHub. If you have any further questions or need assistance, feel free to ask!


##//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

## To learn more about Gitlab, you can continue below

## Add your files

- [ ] [Create](https://docs.gitlab.com/ee/user/project/repository/web_editor.html#create-a-file) or [upload](https://docs.gitlab.com/ee/user/project/repository/web_editor.html#upload-a-file) files
- [ ] [Add files using the command line](https://docs.gitlab.com/ee/gitlab-basics/add-file.html#add-a-file-using-the-command-line) or push an existing Git repository with the following command:

```
cd existing_repo
git remote add origin https://gitlab.com/ray_test_group/ray-test-project.git
git branch -M main
git push -uf origin main
```

## Integrate with your tools

- [ ] [Set up project integrations](https://gitlab.com/ray_test_group/ray-test-project/-/settings/integrations)

## Collaborate with your team

- [ ] [Invite team members and collaborators](https://docs.gitlab.com/ee/user/project/members/)
- [ ] [Create a new merge request](https://docs.gitlab.com/ee/user/project/merge_requests/creating_merge_requests.html)
- [ ] [Automatically close issues from merge requests](https://docs.gitlab.com/ee/user/project/issues/managing_issues.html#closing-issues-automatically)
- [ ] [Enable merge request approvals](https://docs.gitlab.com/ee/user/project/merge_requests/approvals/)
- [ ] [Set auto-merge](https://docs.gitlab.com/ee/user/project/merge_requests/merge_when_pipeline_succeeds.html)

## Test and Deploy

Use the built-in continuous integration in GitLab.

- [ ] [Get started with GitLab CI/CD](https://docs.gitlab.com/ee/ci/quick_start/index.html)
- [ ] [Analyze your code for known vulnerabilities with Static Application Security Testing(SAST)](https://docs.gitlab.com/ee/user/application_security/sast/)
- [ ] [Deploy to Kubernetes, Amazon EC2, or Amazon ECS using Auto Deploy](https://docs.gitlab.com/ee/topics/autodevops/requirements.html)
- [ ] [Use pull-based deployments for improved Kubernetes management](https://docs.gitlab.com/ee/user/clusters/agent/)
- [ ] [Set up protected environments](https://docs.gitlab.com/ee/ci/environments/protected_environments.html)

***
