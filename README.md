# papercool

Use this template directory to write the coolest paper on the internet. 

## Process 

Begin by using this repository as a template to create a new private repository for your paper. 
The new repo is to be created within the ertekin-research-group organization. 

There are four phases: 
  - phase 1: identify paper theme, write the abstract, and make the figures. 
  - phase 2: outline your paper around the figures. 
  - phase 3: fill in the text to make a coherent document 
  - phase 4: finalize items required for paper submisssion. 
  
The phases are tied to issues, which you should track using ZenHub. 

For each phase, you will complete the necessary tasks and carry out the required reviews with your review team. 
You should work with your review team until everyone believes that all the required elements for the phase are in place.  
At this point, you can submit the materials to me for review via your repository. 

## Step by Step Guide (in case you are new to this process) 

1) Create a github account for yourself and send me your id so I can invite you to the ertekin-research-group organization. 

2) Look at [the guide](https://guides.github.com/), especially [Understanding the GitHub flow](https://guides.github.com/introduction/flow/) and [Hello World](https://guides.github.com/activities/hello-world/).  

3) Once you have been invited to ertekin-research-group, install [ZenHub](https://www.zenhub.com/) as a broswer extension. 
This is free for academic use. 

4) Go to the papercool repository and click on 'use this template' to create the repository for your paper. 
Select 'ertekin-research-group' as the owner, and give your repository a short but descriptive name that indicates the year, paper author, and topic (e.g. 2019-Elif-OnCats). Make the repository private. By default, this repository has one branch named 'master'. This will be the main branch for your paper. 

5) Copying a template directory does not have the option to copy over the issues associated with the template directory.  Sadly, this needs to be done manually.  You can do it using from the command line on your terminal using [gh-misssue](https://github.com/E3V3A/gh-missue), a nice set of ruby scripts that lets you use APIs for this purpose. You have to: 

  - install the ruby scripts on your local system. Follow the instructions for installing the scripts carefully.  You need to install ruby, docopt, and octokit. 
  - create a github token for yourself: on github, click on your profile, select settings, and then 'Developer Settings'.  Then choose 'generate new token' and under notes give a name to this token such as 'copy over repo issues'.  Select the box for 'repo' for full control of private repositories. Scroll to the bottom and click on generate token.  Keep track of the token you generate. 
  - in your new repo on github, click on 'issues' and then 'labels' and one by one manually delete all the default labels. There should be no labels left. 
  - back to your command line. copy the labels from papercool to your new repo: 

    gh-missue/gh-missue.rb  -c your_token_here  ertekin-research-group/papercool ertekin-research-group/your_new_repo_here 

  - finally, copy the issues from papercool to your new repo (be patient, this seems to be slow): 

    gh-missue/gh-missue.rb your_token_here -t open ertekin-research-group/papercool ertekin-research-group/your_new_repo_here 
    
  - check on github that the issues and labels appear in your new repo 

    Stuck?  Ask me and I can do it for you once you have created your repo. Have a better solution?  If so, please let me know. 

6) Once the labels and issues have been copied over, go to your repo on github select the ZenHub tab. Switch your workspace to 'Writing a Cool Paper'. For eacah pipeline, you can select the settings tab and choose 'sort by milestone', which should make the phases appear roughly in order.  

7) Clone the repo to your local computer and work here together with your review team. Commit and push your changes often. Once you are satisfied that the materials are ready for review by me for each phase, let me know and I will look them over. 

## Template files provided and integration with overleaf

The example .tex, .bib, and .pdf files included here could be used as a starting point, if you wish.  They need not be used.  The document classs 'achemso' is from the American Chemical Society.  Depending on what journal you are intend to submit your work, you may wish to change this.  It can always be changed later. 

If you want to sync your github repo to overleaf, see [these instructions](https://www.overleaf.com/learn/how-to/How_do_I_connect_an_Overleaf_project_with_a_repo_on_GitHub,_GitLab_or_BitBucket%3F).  You may need to [request authorization](https://help.github.com/en/articles/requesting-organization-approval-for-oauth-apps) to import repos from ertekin-research-group. 


## Why are we doing this? 

I have realized that (i) writing a technical paper is a process, and (ii) the process requires a lot of tacit (meaning understood or implied without being explicitly stated) knowledge. This is my attempt to provide some structure and guidelines for the process, as well as to codify or be explicit about the elements of writing a good paper. 
