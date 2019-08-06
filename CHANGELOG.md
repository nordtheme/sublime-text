<p align="center"><a href="https://www.nordtheme.com/ports/sublime-text" target="_blank"><img src="https://raw.githubusercontent.com/arcticicestudio/nord-docs/develop/assets/images/ports/sublime-text/repository-hero.svg?sanitize=true"/></a></p>

<p align="center"><a href="https://www.nordtheme.com/docs/ports/sublime-text" target="_blank"><img src="https://img.shields.io/github/release/arcticicestudio/nord-sublime-text.svg?style=flat-square&label=Docs&colorA=4c566a&colorB=88c0d0&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgaGVpZ2h0PSIxNiI%2BCiAgICA8cGF0aCBmaWxsPSIjZDhkZWU5IiBkPSJNMTMuNzQ2IDIuODEzYS42Ny42NyAwIDAgMC0uNTU5LS4xMzNMOCAzLjg0OGwtNS4xODgtMS4xOGEuNjY5LjY2OSAwIDAgMC0uNTcuMTMzLjY3Ny42NzcgMCAwIDAtLjI0Mi41MzF2OC4xMzNjLS4wMDguMzIuMjEuNTk4LjUyLjY2OGw1LjMzMiAxLjE5OWguMjk2bDUuMzMyLTEuMmEuNjY4LjY2OCAwIDAgMCAuNTItLjY2N1YzLjMzMmEuNjU5LjY1OSAwIDAgMC0uMjU0LS41MnpNMy4zMzIgNC4xNjhsNCAuODk4djYuNzY2bC00LS44OTh6bTkuMzM2IDYuNzY2bC00IC44OThWNS4wNjZsNC0uODk4em0wIDAiLz4KPC9zdmc%2BCg%3D%3D"/></a></p>

<p align="center"><a href="https://www.sublimetext.com/blog/articles/sublime-text-3-point-1" target="_blank"><img src="https://img.shields.io/static/v1.svg?style=flat-square&label=Compatibility&message=%3E%3D3.1.0%20Build%203170&logo=sublime-text&logoColor=eceff4&colorA=4c566a&colorB=88c0d0"/></a></p>

<p align="center">Changelog for <a href="https://www.nordtheme.com/ports/sublime-text">Nord Sublime Text</a> — An arctic, north-bluish clean and elegant <a href="https://www.sublimetext.com" target="_blank">Sublime Text</a> color theme.</p>

<!--lint disable no-duplicate-headings-->

# 0.1.0

![Release Date: 2019-08-06](https://img.shields.io/static/v1.svg?style=flat-square&label=Release%20Date&message=2019-08-06&colorA=4c566a&colorB=88c0d0) [![Project Board](https://img.shields.io/static/v1.svg?style=flat-square&label=Project%20Board&message=0.1.0&logo=github&logoColor=eceff4&colorA=4c566a&colorB=88c0d0)](https://github.com/arcticicestudio/nord-sublime-text/projects/2) [![Milestone](https://img.shields.io/static/v1.svg?style=flat-square&label=Milestone&message=0.1.0&logo=github&logoColor=eceff4&colorA=4c566a&colorB=88c0d0)](https://github.com/arcticicestudio/nord-sublime-text/milestone/1)

This is the initial release version that mainly focused on the **deployment to the [Package Control][pc] registry** and the [transition to „Nord Docs“][gh-21].

## Features

**Nord Docs Transition** — #21 ⇄ #23 (⊶ 8d01b886)
↠ Transferred all documentations, assets and from „Nord Sublime Text“ to [Nord Docs][nord]
Please see the [corresponding issue in the Nord Docs repository][nord-docs#171] to get an overview of what has changed for _Nord Sublime Text_ and what has been done to migrate to Nord Docs.

###### Landing Page

<p align="center"><a href="https://www.nordtheme.com/ports/sublime-text" target="_blank"><img src="https://user-images.githubusercontent.com/7836623/62528962-fe459680-b83d-11e9-8d54-89f8625ce1af.png" alt="Preview: Nord Sublime Text Port Project Landing Page"/></a></p>

###### Landing Page Docs

<p align="center"><a href="https://www.nordtheme.com/docs/ports/sublime-text" target="_blank"><img src="https://user-images.githubusercontent.com/7836623/62528548-4f08bf80-b83d-11e9-9315-73788f63e9a5.png" alt="Preview: Nord Sublime Text Docs Project Landing Page"/></a></p>

###### Installation & Activation Docs

<p align="center"><a href="https://www.nordtheme.com/docs/ports/sublime-text/installation" target="_blank"><img src="https://user-images.githubusercontent.com/7836623/62528550-4fa15600-b83d-11e9-84be-a58782e3ef1c.png" alt="Preview: Nord Sublime Text Docs Installation & Activation Docs Page"/></a></p>

###### Package Development Docs

<p align="center"><a href="https://www.nordtheme.com/docs/ports/sublime-text/development" target="_blank"><img src="https://user-images.githubusercontent.com/7836623/62528549-4fa15600-b83d-11e9-8c25-481653380cf6.png" alt="Preview: Nord Sublime Text Docs Package Development Docs Page"/></a></p>

**Transition to new JSON based syntax color scheme format** — #22/#1 ⇄ #24/#20/#2 (⊶ 294ab7cf) co-authored by [@kaine119][gh-user-kaine119]
↠ As of [Sublime Text version 3.1.0 Build 3149][sbt-blog-announce-v3.1], a new [JSON based color scheme format `.sublime-color-scheme`][pc-docs-color_scheme] was introduced for easier editing, customization and addition of new features.
Nord migrated to the new format (JSON) from the now [deprecated/legacy `.tmTheme` format][pc-docs-tmtheme] (XML).

> Please note that **Nord now requires a minimum Sublime Text version of [3.1.0 Build 3170][sbt-blog-announce-v3.1]!**

All versions greater or equal to 3.1 build 3120 come with a builtin tool to convert legacy themes to the new format through the command palette when the files is opened in the editor („Convert Color Scheme“).

The following additional changes and additions for features that have been introduced with the new JSON color scheme format are included:

- Added all Nord colors as variables to the `variables` object that are exposed through Sublime Text's internal CSS color scheme API to reuse them with the CSS `var()` function for the defined scope rules.
- Added additional syntax-specific variables to the `variables` object to ensure a uniform color usage for scopes with the same context as well as reducing code duplication and possible transmission errors.
- Added the new Git gutter diff keys `line_diff_added`, `line_diff_modified` and `line_diff_deleted` to the `globals` object to ensure they match Nord's style.

The now [officially deprecated `.tmTheme` color scheme format file][pc-docs-tmtheme] has been removed and is not supported by the Nord theme package anymore.

## Improvements

### Syntax

**Comment Color Brightness** — #18 ⇄ #19 (⊶ 7e388f2e)
↠ Implemented the frequently requested and long-time outstanding increase of the comment color (`nord3`) brightness by 10% from a lightness level of ~35% to ~45%.

➜ **Please see [arcticicestudio/nord#94][nord#94] for all details about this design change decision**!

<p align="center"><strong>Before</strong></p>
<p align="center"><img src="https://user-images.githubusercontent.com/7836623/54902736-76886c80-4eda-11e9-86cd-dfc935aff5e3.png" /></p>
<p align="center"><img src="https://user-images.githubusercontent.com/7836623/54902735-76886c80-4eda-11e9-9aa0-41ded647bdb2.png" /></p>

<p align="center"><strong>After</strong></p>
<p align="center"><img src="https://user-images.githubusercontent.com/7836623/54902766-856f1f00-4eda-11e9-897a-9b0971586a0b.png" /></p>
<p align="center"><img src="https://user-images.githubusercontent.com/7836623/54902765-856f1f00-4eda-11e9-9d09-50c89faece43.png" /></p>

Please see the official documentation about [user and workspace settings][vscode-docs-settings] for more details how to customize and configure VS Code.

## Tasks

### Documentation

**Migration to MIT license** — #4 ⇄ #5 (⊶ 0f1657da)
↠ Adapted to the MIT license migration of [Nord][]. Details can be found in the main task ticket [arcticicestudio/nord#55][nord#55].

<!--
+------------------+
+ Symbol Reference +
+------------------+
↠ (U+21A0): Start of a log section description
— (U+2014): Separator between a log section title and the metadata
⇄ (U+21C4): Separator between a issue ID and pull request ID in a log metadata
⊶ (U+22B6): Icon prefix for the short commit SHA checksum in a log metadata
-->

<!--lint disable final-definition-->

<!-- Base Links -->

[nord]: https://www.nordtheme.com
[pc-docs-color_scheme]: https://www.sublimetext.com/docs/3/color_schemes.html
[pc-docs-tmtheme]: https://www.sublimetext.com/docs/3/color_schemes_tmtheme.html
[pc]: https://packagecontrol.io

<!-- v0.1.0 -->

[gh-21]: https://github.com/arcticicestudio/nord-sublime-text/issues/21
[gh-user-kaine119]: https://github.com/kaine119
[nord-docs#171]: https://github.com/arcticicestudio/nord-docs/issues/171
[nord#55]: https://github.com/arcticicestudio/nord/issues/55
[nord#94]: https://github.com/arcticicestudio/nord/issues/94
[sbt-blog-announce-v3.1]: https://www.sublimetext.com/blog/articles/sublime-text-3-point-1
