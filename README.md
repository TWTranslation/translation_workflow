---
tags: ttw
---

[TOC]

# *The Turing Way* translation workflow

[![hackmd-github-sync-badge](https://hackmd.io/_qLIaz9aRcCBUMmvc5Drdg/badge)](https://hackmd.io/_qLIaz9aRcCBUMmvc5Drdg)


**Note** This is work in progress and some of these steps may change in the future. You can contact anyone on the `#translation` channel in *The Turing Way*  Slack space.

## Repository and organization

Our current Translation Management System is [Crowdin](https://turingway.crowdin.com/). 
Crowdin is integrated to a GitHub fork of *The Turing Way* in a **temporary** [GitHub  Organization](https://github.com/TWTranslation/the-turing-way).
Every time the repository is updated, Crowdin starts an automatic translation.
These translations need to be reviewed and accepted before being considered final.

## Before starting a new language 

In Crowdin, check The Turing Way project. This print shows it has seven target languages at the moment: 

![The Turing Way project in Crowdin](https://i.imgur.com/ebepaIw.png)

Check if the language you want to translate to is already present or if you need to [add a new language](adding-a-new-language)


## Adding a new language

To add a new language, click on the three dots on the top right corner and click on "Target languages". In the search field look for the new target language.
![Click on target languages](https://i.imgur.com/zXipQy5.png)

In this example, we added Brazilian Portuguese to the list

![Add the selected language](https://i.imgur.com/Q55H0HG.png)

When adding new languages, they have no assigned coordinators, anyone can be assigned at any moment

![](https://i.imgur.com/RSKjj6j.png)
![](https://i.imgur.com/N5vtA5C.png)

## Workflow steps 
In Project home > Translations > Workflow, you can see the whole translation workflow, with automatic steps (TM Pre-translation and MT Pre-translation) and steps that need human input or revision (Translation, Proofreading). 


![](https://i.imgur.com/GC7rUWy.png)



When a language is added, Crowdin will start the automatic translation processes, either via translation memory or machine translation.

## Review translations

In the translation step, the translator will review the output of the automatic translation and modify or accept the suggested translations.

You can browse the content by strings or by files, we recommend browsing it by file so that entire sections of *The Turing Way* are translated in context.

In Project Home you will see the list of languages, when clicking your language, a list of files and their current status will appear.

![](https://i.imgur.com/upKET1k.png)
![](https://i.imgur.com/kdmd657.png)

In blue, you can see the completion status of the automatic translation. 
It can be close to 100% because some strings are not automatically translated. 

In this example, the selected file was 92% translated automatically and no translation has been approved.
The next steps are 1. translating the missing strings and 2. approve them all
![](https://i.imgur.com/pDoj66r.png)

When a file has been completely translated and approved, it will be marked in green. 


![](https://i.imgur.com/fRj4Yn3.png)



Now let's see how this translation and approval works

## Translate missing strings and approve translations

Select the file you want to work on. 
Remember the structure of this repository is exactly as The Turing Way so there are five guides with overview files and content files inside subfolders.

![The Turing Way project illustration by Scriberia. Zenodo. http://doi.org/10.5281/zenodo.3695300](https://the-turing-way.netlify.app/_images/theturingway-chapters.jpg)

The editor menu has two modes, translation and proofreading, you can use translation mode to translate missing strings and proofreading mode to check all the translations
![](https://i.imgur.com/yQcxszA.png)
![](https://i.imgur.com/HNt5SfE.png)

### Proofreading mode
Proofreading mode will show you the original string, the current translation and some options proposed by crowdin.
When a string matches past translations, these past translations will appear among the options.

You can either choose one of these or edit directly in each string's field.
When you reach a satisfactory translation, click on Save.

![](https://i.imgur.com/drLjzTC.png)

On the top there are some filters to show which strings are translated or untranslated and approved or not 

#### Some tips

Do not translate: 
- Python book tags `(#welcome)=`
- Relative file paths
- Fields `name:` and `alt:` in images (do translate the alternative text, though)

Check for modifications in:
- References 
- Tag and variable order ex: `{ref}<0>text</0>` should have the same structure