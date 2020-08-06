# Demo Days - Browser Camera Action

- [ ] TODO insert demo days logo
- [ ] Make a badge for our action
- [ ] publish our action to the market place

#### <a alt="Too Long; Don't Read;">TL;DR;</a>

We will be building a GitHub Action using javascript (node.js) and interacting with various pieces of functionality exploring some of the art of the possible, If all goes well and hurricane ISAIAS hasn't taken out the power :zap: :boxing_glove: then I'll be showing off GitHubs new Cloud Development Environment (CDE ... :man_shrugging: feelse a [little overloaded](https://acronyms.thefreedictionary.com/CDE) but hey) otherwise known as **codepsaces**</sup>

I'm working on the theory that most folk's attending the live twitch are familiar with `git` and :octocat: GitHub, and that most folks are :cool: with **creating branches, creating and merging pull requests** and not :fearful: a little command-line git

I'll be working from a  Mac but you can run follow along on a system of your choice - if you are lucky enough to be part of the codespaces beta - you can even try following along with just a tablet ... ( a phone might be a little ambitious and a sub-optimal experience)

---

Steps we're going to attempt

**Step 1. A simple workflow...**

- [ ] Create a new GitHub Repository and initialize with a README.md
- [ ] Add our initial workflow (it will run our action) ... we'll need a few things
   - [ ] A workflow file `.github/workflow/main.yml`
   - [ ] let's run with just a `script` to :mega: `echo` first 

:information_source: now is a good time to discuss actions basics, eco-system and some of the cool extensions in CDE/Codespace  
Also the amazing eco-system of actions for all manor of things that already exists 

<details><summary>snippets</summary>

.github/workflows/main.yml
```yml
name: demo days javascript action
on: 
  push:
    branches:
      - .*-test$
jobs:
  hello-world-job:
    runs-on: ubuntu-latest
    steps:
      name: hello world
        run: | 
          echo "hello world"
```

**Step 2. - Building on Step 1. with javascript and index,js**

- [ ] install our @actions/core and @actions/github packages
``` sh
npm install @actions/core
npm install @actions/github
``` 
- [ ] An `action.yml` that describes our action
- [ ] Add Some code to `index.js` that doesn't ... break stuff ... `console.log("hello")`
- [ ] turn on actions debugging :secret: `ACTIONS_STEP_DEBUG` set to `TRUE`
- [ ] log out the event context and see what's there
- [ ] the ubiquitous `hello-world`

good time to talk about secrets, vaults integration, and some security considerations

**step 3. Upload an artifact**
- [ ] write the context information to file (standard IO)
- [ ] import the actions artifact (require) 
- [ ] trigger the action and download our artifact

**step 4. Adding files to the repo** 
- [ ] add a `run` job to our existing action
- [ ] use some simple commands to set up our git client and push some code 
- [ ] go see our repo 

---


:smiling_imp: Devil in the Detail :smiling_imp:


## Code Along Resources

- This repository for starters :)
- [VSCode Download](https://code.visualstudio.com/download)
- [GitHub signup - just in case you don't have one yet](https://github.com/join)
- [node and npm - for your OS](https://www.npmjs.com/get-npm) - unless you have codespaces of course ;) **version 12.x.x**
- [Online Git Reference](https://git-scm.com/doc) - for the curious and the studious
- [GitHub Emojis](https://github.com/onmyway133/emoji) You'll probably want to lighten the mood a little :moon::sparkles::sunrise::coffee:
- [Mastering Markdown](https://guides.github.com/features/mastering-markdown/) ... in case documentation is your thing 


---

### :information_source: Information, Docs, Tutorials and More


- [Code Spaces](https://github.com/features/codespaces/)  - GitHub CDE (Cloud Development Environment)  (_not Cutest Dog Ever_))
  - sign up for the Beta on :point_up: on this page
  - see [documentation](https://docs.github.com/en/github/developing-online-with-codespaces) on GitHub Docs
  - dotFiles [for codespaces](https://docs.github.com/en/github/developing-online-with-codespaces/personalizing-codespaces-for-your-account) or for everything GitHub [:heart: ~/.](https://dotfiles.github.io/) - and yes - the :heart: emoji is a hyperlink  
- GitHub Actions 
  - Actions intro and [help docs on GitHub Docs](https://docs.github.com/en/actions)
  - [Creating Actions](https://docs.github.com/en/actions/creating-actions)
  - [Official GitHub Tutorial for JavaScript Action](https://docs.github.com/en/actions/creating-actions/creating-a-javascript-action)
  - [Workflow Syntax Documentation](https://docs.github.com/en/actions/reference/workflow-syntax-for-github-actions)
  - [Actions Toolkit Library](https://github.com/actions/toolkit) 
  - [Actions API (v3)](https://developer.github.com/v3/actions/)
  - [Tools included on hosted runners](https://docs.github.com/en/actions/reference/software-installed-on-github-hosted-runners)
  - [Metadata syntax for actions](https://docs.github.com/en/actions/creating-actions/metadata-syntax-for-github-actions)

- GitHub API 
  - [Developer Documentation](https://developer.github.com/) V3 and V4 (GraphQL for those who like living on the "edge")
  - [Octokit](https://github.com/octokit) and  [octokit/rest.js](https://github.com/octokit/rest.js/) wrapper for GitHub API
  - **hot off the press** the [actions workflow usage endpoints](https://developer.github.com/changes/2020-05-15-actions-api-workflow-usage/)

And if I really did a terrible job today - and you'd rather __not speak to a human__

- Actions learning lab - practical bot driven tutorial  
![actions learning lab](images/actions-learning-lab-signup.png)

