# Onboarding Guide

## Core Requirements
* Other people can edit this guide, which needs to be version controlled.
* The guide is easily accessible.
* Particular sections of the guide can be linked to and shared.

## Instructions
* To build, use `npm run build`.
* To run, use `npm run serve`.
* The [sidebar is constructed](https://honkit.netlify.app/pages.html) using `SUMMARY.md`.
* HonKit [builds the glossary](https://honkit.netlify.app/lexicon.html) with the contents of the `Glossary.md` file. The pattern for defining terms is as follows:
```
## Term
Definition for this term
```

**Note**: this particular README is not used by honkit in the build. `docs` folder contains the markdown files used by honkit in the build step as configured by `book.json`.