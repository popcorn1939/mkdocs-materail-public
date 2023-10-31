# Page 4

# Setting Up a Python Project on macOS with GitHub and pyenv



## Table of Contents
- [Step 0: Install and setup MKDocs](#step-0-install-and-setup-MKDocs)
- [Step 1: Install and Setup pyenv](#step-1-install-and-setup-pyenv)
- [Step 2: Create a Local Python Project](#step-2-create-a-local-python-project)
- [Step 3: Initialize a Git Repository](#step-3-initialize-a-git-repository)
- [Step 4: Create a Repository on GitHub](#step-4-create-a-repository-on-github)
- [Step 5: Connect Local Repository to GitHub and Push](#step-5-connect-local-repository-to-github-and-push)



## Step 0: Install and Setup MKDDocs

1. **New repository from GIT**
   ```bash
   Press new repository
   define a name: mkdocs-material-tutor
   mkdocs-materail-public
   description: <blanc>
   Private
   Add a README file
   gitignore: python
   licence: GNU Public License
   Create reposity
   ```

2. **download repository and install virtuel environment**
   ```bash
   copy the SSH command

   https://github.com/popcorn1939/mkdocs-materail-public.git
   Macos Terminal:git clone ..paste ssh command
   cd to the new project created
   pyenv local 3.9.16
   python3 -m venv ./
   source bin/activate

   pip --version - to check if pip is installed
   ls -al
   pip install mkdocs-material
   pip install "mkdocs-material[imaging]"

   code .   # starts Visual studio code
   ```
3. **VSC - Init mkdocs serve environment**
   ```bash
   start terminal within VSC
   mkdocs new .
   mkdocs serve
   Open chrome and paste the url
   ```

4. **VSC - Install Material Plugin**
   ```bash
   edit mkdocs.yml and include theme -> name: material
   #følgende melding kommer: AttributeError: 'SearchPlugin' object has no attribute 'is_dirty'
   mkdocs serve  #ignorrer feil melding og tast kommenoen
   Open chrome and paste the url

   mkdocs new .
   mkdocs serve
   Open chrome and paste the url
   ```

    


200. **prepare github actions and upload to repository**
   ```bash
      mkdir .github
      cd hithub
      mkdir workflows
      cd workflows
      new file... ci.yml
      Edit the ci.yml  #bunden av filen 
   ```

201. **upload to repository**
   ```bash
      start terminal in vsc
      git add .
      git commit -m $'Adding initial documentation files'
      git push origin main
   ```

202. **Go to github og publish dokumentene til github.io ...**
   ```bash
      refresh page # you will see the uploaded files
      go to "settings" -> click "Pages" on the left side
      "source" -> settes til "Deploy from the branch
      "branch" -> settes til "git-pages". Etterpå velg save
      "Actions" - velges fra hovedmenu. Click "ci" on the left side. Nu ser der et "workflow
      "Run mkdocs gh-deploy --force". Ettepå fås melding "Your documentation should shortly be availle at ...."
      Nu kan dokumentetene læses fra dit githubio






   ```


   define a name: mkdocs-material-tutor
   description: <blanc>
   Private
   Add a README file
   gitignore: python
   licence: velg 
   Create reposity
   ```


## Step 1: Install and Setup pyenv

![pyenv Logo](https://www.rosehosting.com/blog/wp-content/uploads/2020/11/pyenv-logo.png)

1. **Install pyenv**
   ```bash
   brew install pyenv
   ```

2. **Add pyenv to bash so that it loads every time you open a Terminal**
   ```bash
   echo 'if command -v pyenv 1>/dev/null 2>&1; then eval "$(pyenv init --path)"; fi' >> ~/.zshrc
   ```

3. **Restart your shell**
   ```bash
   exec "$SHELL"
   ```

4. **Install Python 3.9.16 using pyenv**
   ```bash
   pyenv install 3.9.16
   ```

## Step 2: Create a Local Python Project

![venv Logo](https://docs.python.org/3/library/venv-logo.png)

1. **Navigate to the directory where you want to create your project**
   ```bash
   cd path_to_your_directory
   ```

2. **Create a new directory for your project and navigate into it**
   ```bash
   mkdir my_lazy_doc
   cd my_lazy_doc
   ```

3. **Set the local Python version for your project to 3.9.16**
   ```bash
   pyenv local 3.9.16
   ```

4. **Create a new virtual environment named `venv39` using the specified Python version**
   ```bash
   python3 -m venv venv39
   ```

5. **Activate the virtual environment**
   ```bash
   source venv39/bin/activate
   ```

## Step 3: Initialize a Git Repository

![Git Logo](assets/images/git.png)


1. **Initialize a new Git repository in your project directory**
   ```bash
   git init
   ```

2. **Create a `.gitignore` file and add necessary files/directories to be ignored**
   
   ```bash
   touch .gitignore
   nano .gitignore
   ```
3. **Go to gitignore.io and select Python. Add the output code to the .gitignore**

   ```
   venv39/
   __pycache__/
   ```

## Step 4: Create a Repository on GitHub

![Github Logo](assets/images/github.jpeg)




- **Go to GitHub and create a new repository named `my_mark`**
- **Don’t initialize the repository with a README, .gitignore, or License.**

## Step 5: Connect Local Repository to GitHub and Push

1. **Connect your local repository to your GitHub repository**
   ```bash
   git remote add origin https://github.com/popcorn1939/my_mark.git
   ```

2. **Add files, commit, and push to GitHub**
   ```bash
   git add .
   git commit -m "Initial commit"
   git push -u origin master
   ```



## Step 6: Install JupyterLab and do a test

1. **Show installed libraries**

   ```bash
   pip list
   pip install jupyterlab
   ```

2. **Run JupyterLab**

   You can start JupyterLab (http://localhost:8888/lab) by running the following command in your terminal:

   ```bash
   jupyter lab
   ```

3. **Start Terminal from JupyterLab**

   Ensure you have the right envirenment (http://localhost:8888/lab) by running the following command in your terminal:

   ```bash
   python version
   pip list
   pwd
   ```
   
   





## Step 7: Install python-dotenv

Incorporate the `python-dotenv` package to manage sensitive information in your `basic_start` project

1. **Install `python-dotenv` using `pip`:**

   ```bash
   pip install python-dotenv
   ```

2. **Create a `.env` File**

   ```bash touch .env
   touch .env
   nano .env
   ```
	- Open `.env` and add sensitive data as key-value pairs:
   
   ```bash
   SECRET_KEY=mysecretkey
   API_TOKEN=myapitoken
   ```
   
   

## Step 7: Install panel

Incorporate the `python-dotenv` package to manage sensitive information in your `basic_start` project

1. **Install `panel` using `pip`:**

   ```bash
   pip install panel
   ```

2. **Create a `.env` File**

   ```bash touch .env
   touch .env
   nano .env
   ```

   - Open `.env` and add sensitive data as key-value pairs:

   ```bash
   SECRET_KEY=mysecretkey
   API_TOKEN=myapitoken
   ```

   
