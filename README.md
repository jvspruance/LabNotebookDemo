# LabNotebookDemo
Contains suggestions/guidance for organizing a Github-based lab notebook.

The organization system is inspired by a couple of sources:
- https://bioinformatics.stackexchange.com/questions/112/how-to-version-the-code-and-the-data-during-the-analysis
- https://alexllc.github.io/posts/organization/
- https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1006918
- https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1000424

## Usage

The notes file structure is somewhat easy to navigate, as each experiment is dated and labeled with the type of work/experiment being conducted. However, it may be more useful to use a table of contents (`TOCbyProject.md`, `TOCbyDate.md`) to navigate notes.

I have found that maintaining multiple projects in the same repo (especially if they are very different) is challenging, and will grow very quickly. It is kind of personal preference whether projects should get their own independent repos or not, and this decision should affect folder hierarchy. 

- Each project has a list of experiments. Each experiment has a list of notebook entries. Each entry will consist of a folder.

Each notebook entry should explain **what** I did and **when**, **why** and **how** I did it. This information is stored in a Markdown file with the following format:

1) **Title**
2) **Background/motivation**
    * What is the project at a very high level? Why am I doing this analysis?
3) **Objective(s)**
    * What are the goals for this experiment?
4) **Materials and Methods**
   * If any of my own project repos/tools were used to perform this experiment, what was the most recent commit?
   * If any external tools were used to perform this experiment, what versions were used?
        * i.e. SAMtools, cloned repos, etc.
    * What config/environment was used to perform this experiment?
    * What genome builds were used to perform this experiment?
    * What data was involved in this experiment? How was it generated?
    * What scripts(s) were run to produce the results in this experiment?
        * For notebooks, provide the most recent commit. For shell scripts, attach a copy of the commands and std.out
5) **Results**
    * Was there data generated during this experiment? If so, what is the filename/path?
    * Was there a figure generated? If so, explain what the figure is showing
6) **Conclusions**
    * If new data was generated, what should it be used for? Why is it important?
    * If a new figure was generated, what does it mean within the context of the project?
    * What are the likely future directions? 

## Data Generation

Github repos can't track changes across large files. Version control is suitable for text documents and scripts, but this quickly becomes untenable for large amounts of data.

To try and keep track of data generation, it is a good rule of thumb to date generated data and store it outside of the repo. The data can then be referenced in the notes for the day that generated the data.

It is also a good idea to keep track of what generated data mean (again, outside of the repo) by leaving a `README.md` in the folder associated with the data. 
