# violene

Project violene is a project to assist researchers to keep track of their experiments and store the results of their experiments in Markdown format. These all results are locally stored and can be exported to markdown formats.

Project Start Date: September 16th, 2024

Author: Biplab Gautam

# white paper

Problem: When doing my Master's thesis I always wanted to keep track of all my experiments in a neat and easily accessible fashion, so that I can make use of it later when I am in thesis writing phase. So, I gave title to each of the experiments, experiment ID, stored the results in table and pictures and then saved all of them in my notion notes. But everytime, I had to do back and forth between my notion notes and my codes in the project.

With project **violene**, our goal is to combine the code writing part of the project and this experiment documentation part and make it seamless. Here are the basic features of project violene.

1. Create a **project**. This project has it’s name, description. For one parent directory, there is one project.
2. Inside a project there are **experiments** (like a collection of experiment runs). A project can have multiple different directions that are being tackled. Each direction are called experiment. Each experiment has it’s name, description. One project can have multiple collections.
3. Then we come to experiment **runs**. Experiment run will be the most fine element that we have in our tracking project.

   1. Run ID (Repo-Experiment-RunID)
   2. Name of experiment run
   3. Description (Basically markdown)
   4. Pictures (More than one)
   5. Tags (Custom created)
   6. Date of experiment (Created, last modified date)
   7. Result in particular

   **SubRun**

   Each run can have **subruns**. And this can go basically like a tree with virtually no limit. But we would definitely recommend users not to go too deep. If it is a subrun then it is going to have the id of it’s parent run and hint in the id that it is a subrun. But we are not going to complicate subruns too much, all subrun will be treated equally like a run and shall be visible inside the topmost run.

4. Associate each source code file with an experiment run. There should be no limit in how many experiment runs a code file has. Since there can be more than one experiment run in a code file also store the line number in the code file for each experiment run.
5. **Export Features**. Since this is basically a documentation project. There should be super easy way to export the docs.
   1. Export into markdown where each of the experiments and their runs are marked and listed properly. It has all the links to the pictures, dates, results, descriptions mentioned like a proper report. Give user the option to have one big markdown file or more than one markdown.
   2. Export into pdf like a report for the above markdown. Kind of like a rendered final version.
6. **VSCode Plugin's Feature**
   1. have a config file in the repo. That config file in json or some simple format. This basically reduces or removes the requirement to have it uploaded or used in a SAAS system. Everytime user commits their code in git, the experiment's docs will also be committed simultaneously.
   2. Connect one run or subrun to a code.
      Gather the comments from the file and build project description automatically.
   3. Be able to take portion of the code like line numbers and allow it in the documentation part.
   4. Be able to drag and drop/paste images/screenshots from code section into the UI of the plugin.
