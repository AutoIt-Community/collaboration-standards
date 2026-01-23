## 1. Contribution guideline

### Purpose

For projects/repositories, there are several common and recommended guidelines which lead to a stable and understandable way of working with code as a team.

One of the main reasons why this guidance and standards exists is consistency for writing code, also for reviewing code. Otherwise all kinds of styles could be exists which would mislead newcomers and would make the start into the project more difficult.

<br>

### 1. Language

- use english for code, comments, branches, tags, commit messages etc.
- do not mix german and english as long as possible
- but also do not translate german specific names (keep them)

<br>

### 2. Branch naming

**Usage**

- use [kebab-style](/docs/en/case-styles.md) for the branch name
  - all lowercase
  - all words separated by the hyphen

**Examples**

- add-database-connection
- add-login-feature
- apply-common-standards
- fix-prototype-code
- project-restructuring
- remove-obsolete-feature
- update-to-specific-version

**Why**

- consistency
- common way to do it

<br>

### 3. Commit-message conventions

**Usage**

- use the "[Keep a Changelog](https://keepachangelog.com/en/1.1.0/)" style
  - \<Keyword\>\<colon\>\<space\>\<Message as a sentence with final punctuation.\>
- Keywords and their purposes
  - **Added** for new features.
  - **Changed** for changes in existing functionality.
  - **Deprecated** for soon-to-be removed features.
  - **Documented** for documentation only changes.
  - **Fixed** for any bug fixes.
  - **Refactored** for changes that neither fixes a bug nor adds a feature.
  - **Removed** for now removed features.
  - **Security** in case of vulnerabilities.
  - **Styled** for changes like whitespaces, formatting, missing semicolons etc.

**Examples**

``` bash
git commit -m "Added: Three-part statusbar to the main GUI."
git commit -m "Changed: Sort logic to DESC order instead of ASC."
git commit -m "Fixed: Broken label by set correct attribute."
git commit -m "Refactored: Usage of map data type instead of array."
```

**Why**

- consistency
- beside "[conventional commits](https://www.conventionalcommits.org/en/v1.0.0/)" (cc) is the "Keep a Changelog" style another common way (more easy and more human readable than cc) to deal with
- CHANGELOG.md file can be generated automatically when creating a new release

<br>

### 4. Pull requests (merge requests)

- do not force push into main (default) branch
- do create a merge request of your feature branch into main
- wait for the code review approval, then merge your code into main [^1]

### 5. Code review

To be defined.

<br>

### 6. Version bump (SemVer)

To be defined.

<br>

### 7. Changelog

To be defined.

<br>

### 8. Releases and Tags

**Usage**

- use git tags for the release version
- use simple [SemVer](https://semver.org/) tag names like `v0.13.2` or `v4.1.0`
- do not use prefixes or suffixes for the release tags
  - prefixes can be used for all other tags like "hotfixes" oder "MVPs"
  - if prefixes or suffixes, use lowercase and use [kebab-style](/docs/en/case-styles.md)

**Creation example**

See [this](https://github.com/Sven-Seyfert/au3webdriver-boilerplate/releases) example release structure.

| Choose a tag | Release title        | Release description |
| ---          | ---                  | ---                 |
| v0.13.2      | v0.13.2 - 2024-02-20 | Either copy the changelog information of the new release into the 'Release description' section. Or reference to the CHANGELOG.md file like "see CHANGELOG.md file" or similar. |

**Why**

- consistency
- each release version is a stable working version

<br>

---

## 🔗 more topics

### [Workflows and how-tos](/docs/en/workflows-how-tos.md)

<br>

---

Footnotes
[^1]: Approval process has to be configured for each GitHub repository.
