# Organizing a Version-Controlled Lab Notebook

See today's README in the parent directory for general guidelines regarding lab notebook organization.

I want to set up a very rigorous note-taking framework that covers all of my experimental methods, my thoughts/what I'm reading, and tracks file changes to facilitate easy reproducibility and sharing of my progress. 

I will continue to take *some* notes in OneNote because it allows me to sketch/draw things out, but OneNote is definitely not an ideal, unified framework for tracking my work because it's very separate from my code. 

I think that storing my notes in a git repo is in my best interests for a couple of reasons:
1) I can access these notes from any device, and they are backed up. I don't need to be <u>in</u> lab working on respublica in order to access my notes
2) Version control lets me figure out when I changed my scripts. I don't need to make many versions of the same script, I can just revert back to a previous commit if something gets messed up.
3) It's easy to share these notes. When it comes time to share my notebook with someone else, I can just send them a link.

## Data Provenance
In addition to version-controlling my notes, something I've spent a good time thinking about is data provenance, or datasheets for datasets. 

Each piece of data I generate should have its own accompanying lab notebook entry for future reference.

Whenever I generate a new piece of data, I want to know a couple of things about it:
1) When was it generated
2) When was it last modified (ideally this is the same as when it was generated)
3) Why did I make it
4) How did I make it (i.e. what scripts were run to generate it)
5) What is it/why is it significant

I think that it would be borderline impossible to version control all of the intermediate datafiles that I will inevitably generate through this PhD. The next best thing is to make sure the raw data is backed up (and write datasheets for the raw data) and rigorously document how every other piece of data is generated so it can be made again.

## Pivoting Away from OneNote

I have been taking most of my notes in OneNote up until this point. I still think it's great for handwriting scratch work, but I'm going to pivot away from it for written stuff so I can keep most of my notes in the same place.

I'm going to start converting my OneNote notes that I have remaining to this repo so they're all in the same place. Hopefully this makes searching for things much easier (I could just `grep` a whole folder of notes?)

## Using Zotero

Zotero has been a boon for me since starting this PhD. I have been cataloging all of the papers I've read, leaving annotations and synopses as I go. I hope that this serves as a means for me to quickly gather sources when it comes time to write a paper. It has already been super helpful in keeping track of what I've read and quickly producing bibliographies.