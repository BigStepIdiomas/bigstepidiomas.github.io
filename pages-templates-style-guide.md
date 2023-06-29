---
layout: default
title: Templates - Style Guide
description: What're ya buyin?
---

<style>
.tag {
  display: inline-block;
  padding: 4px 8px;
  border-radius: 4px;
  color: #fff;
  font-size: 14px;
  font-weight: bold;
  margin-right: 8px;
  margin-bottom: 10px;
}

/* Add the background colors for each category */
.tag:nth-child(1) { background-color: #007bff; } /* UX Writing */
.tag:nth-child(2) { background-color: #28a745; } /* Technical Specification */
.tag:nth-child(3) { background-color: #dc3545; } /* API Docs */
.tag:nth-child(4) { background-color: #ffc107; } /* Technical Documentation */
.tag:nth-child(5) { background-color: #6f42c1; } /* Knowledge Base */
.tag:nth-child(6) { background-color: #fd7e14; } /* Translation */
.tag:nth-child(7) { background-color: #20c997; } /* English */
.tag:nth-child(8) { background-color: #e83e8c; } /* Installation Guides */
.tag:nth-child(9) { background-color: #6c757d; } /* Help Docs */
.tag:nth-child(10) { background-color: #17a2b8; } /* Troubleshooting */
.tag:nth-child(11) { background-color: #87ceeb; } /* Handbooks */
.tag:nth-child(12) { background-color: #90ee90; } /* Support Docs */
.tag:nth-child(13) { background-color: #ff6666; } /* Project Docs */
.tag:nth-child(14) { background-color: #ffff99; } /* Portuguese */
.tag:nth-child(15) { background-color: #d291bc; } /* Release Notes */
.tag:nth-child(16) { background-color: #ffb347; } /* German */
.tag:nth-child(17) { background-color: #98d8d8; } /* SDK */
.tag:nth-child(18) { background-color: #ffb6c1; } /* Product Discovery */
.tag:nth-child(19) { background-color: #d3d3d3; } /* UX Design */
.tag:nth-child(20) { background-color: #afeeee; } /* Spanish */
.tag:nth-child(21) { background-color: #cd853f; } /* Copywriting */
.tag:nth-child(22) { background-color: #ffa07a; } /* Microcopy */
.tag:nth-child(23) { background-color: #f08080; } /* Educational Material */
.tag:nth-child(24) { background-color: #da70d6; } /* Localization */
.tag:nth-child(25) { background-color: #8470ff; } /* User Guides */
</style>

<span class="tag" style="background-color: #007bff;">UX Writing</span>
<span class="tag" style="background-color: #28a745;">Technical Specification</span>
<span class="tag" style="background-color: #dc3545;">API Docs</span>
<span class="tag" style="background-color: #ffc107;">Technical Documentation</span>
<span class="tag" style="background-color: #6f42c1;">Knowledge Base</span>
<span class="tag" style="background-color: #fd7e14;">Translation</span>
<span class="tag" style="background-color: #20c997;">English</span>
<span class="tag" style="background-color: #e83e8c;">Installation Guides</span>
<span class="tag" style="background-color: #6c757d;">Help Docs</span>
<span class="tag" style="background-color: #17a2b8;">Troubleshooting</span>
<span class="tag" style="background-color: #87ceeb;">Handbooks</span>
<span class="tag" style="background-color: #90ee90;">Support Docs</span>
<span class="tag" style="background-color: #ff6666;">Project Docs</span>
<span class="tag" style="background-color: #ff6666;">Portuguese</span>
<span class="tag" style="background-color: #d291bc;">Release Notes</span>
<span class="tag" style="background-color: #ffb347;">German</span>
<span class="tag" style="background-color: #98d8d8;">SDK</span>
<span class="tag" style="background-color: #ffb6c1;">Product Discovery</span>
<span class="tag" style="background-color: #d3d3d3;">UX Design</span>
<span class="tag" style="background-color: #afeeee;">Spanish</span>
<span class="tag" style="background-color: #cd853f;">Copywriting</span>
<span class="tag" style="background-color: #ffa07a;">Microcopy</span>
<span class="tag" style="background-color: #f08080;">Educational Material</span>
<span class="tag" style="background-color: #da70d6;">Localization</span>
<span class="tag" style="background-color: #8470ff;">User Guides</span>

# {Your Project Name} style guide

{Version number and last updated date}

## Introduction

{Before using this template, please read the accompanying About the Style Guide
Template documentation.}

Welcome to our project! This style guide is intended for use by project
contributors, not necessarily end-users. It provides general guidance to anyone
who contributes to the project's documentation.

## Intended audience and scope

This style guide is intended for use by any contributors that are writing
documentation for {Your Project Name}, including software engineers. This guide
can help project contributors to communicate clearly and consistently in {you
define the scope: the project's end-user documentation, API documentation,
forum posts, and so forth.}

## Our preferred style guide

We have adopted the
{[your preferred style guide, such as the Google developer documentation style guide](https://developers.google.com/style)}
for {Your Project} documentation. For a quick summary, see the
[Google style guide highlights](https://developers.google.com/style/highlights).
The rest of this document describes our project-specific customizations to
{Google's or your preferred} guide.

Our project uses {your choice: standard American spelling or standard British
spelling, etc.} and our preferred dictionary is the
{[American Heritage Dictionary](https://ahdictionary.com/) or your preferred
dictionary}.

When writing documentation for our project, align with the default guide's
voice and tone.

## Glossary of preferred terms

{Calling out how to write your project name first is optional. You can choose to include your project name in the word list instead.}

This {Your Project Name} is represented as {example}. It is {always/never}
capitalized.

The table provides guidelines about the terms you should and should not use for
consistency, listed in alphabetical order:

Preferred Term  | Avoid These Terms  |  Explanation
--------------- | -----------------  |  -----------
for example     | e.g.               |  Avoid non-English words
people with disabilities  | <ul><li>the disabled</li><li>disabled people</li><li>people with handicaps</li><li>the handicapped</li></ul>  |  Use inclusive and bias-free language. See [Accessible Writing](#accessible-writing)
that is         |  i.e.              |  Avoid non-English words

## Topic types and templates

This project recommends using the following templates from the
[Good Docs project](https://github.com/thegooddocsproject/templates):

- API Overview
- API Quickstart
- API Reference
- Discussion Article
- How To Guide
- Logging Article
- Reference Article
- Tutorial

## General writing tips

{This section is optional.}

For some general tips about improving writing see:

- [Write the Docs - Style Guides](https://www.writethedocs.org/guide/writing/style-guides/#writing-style)
- [18F Content Guide](https://content-guide.18f.gov/)

## Accessible writing

Documentation should be written in a way that supports people with disabilities
and users with various input methods and devices. Improving accessibility also
helps make documentation clearer and more useful for everyone.

For resources on making your writing more accessible, see:

- [Writing accessible documentation - Google developer documentation style guide](https://developers.google.com/style/accessibility)
- [Accessibility guidelines and requirements - Microsoft Writing Style Guide](https://docs.microsoft.com/en-us/style-guide/accessibility/accessibility-guidelines-requirements)
- [Writing for Accessibility - Mailchimp Content Style Guide](https://styleguide.mailchimp.com/writing-for-accessibility/)

## Inclusive and bias-free writing

When contributing to this project, you should strive to write documentation with
inclusivity and diversity in mind. Inclusive language recognizes diversity and
strives to communicate respectfully to all people. This kind of language is
sensitive to differences and seeks to promote equal opportunities.

For resources on making your writing more inclusive, see:

- [Inclusive documentation - Google developer documentation style guide](https://developers.google.com/style/inclusive-documentation)
- [The Conscious Style Guide - a collection of resources](https://consciousstyleguide.com/)
- [Bias-free communication - Microsoft Writing Style Guide](https://docs.microsoft.com/en-us/style-guide/bias-free-communication)
- [Guidelines for Inclusive Language - Linguistic Society of America](https://www.linguisticsociety.org/resource/guidelines-inclusive-language)

## Using linters

{This section is optional.}

This project uses the {your preferred linter.}

{Provide instructions or policies related to the linter here.}

## How the style guide is updated

{Indicate here how frequently your style guide is reviewed, who owns the style
guide, and how contributors can provide feedback on your style guide.}

## Revision history

{This section is optional or can be combined with the next section if needed.}

The following table describes the history of all decisions and revisions made to
this style guide over time. This guide uses the Major.Minor.Patch
[semantic versioning](https://semver.org/) convention.

Edition  |  Date          |  Lead Author(s)    |  Link to Repository Commit/Tag
-------  |  ----          |  --------------    |  -----------------------------
{0.1}    |  {YYYY-MM-DD}  |  {Your name here}  |  First draft of Style Guide


## Decision log

{This section is optional or can be combined with the previous section if
needed.}

The following table describes the history of all decisions made to this style
guide over time:

Ref  |  Date         |  Description                               |  Agreed to by
---  |  ----         |  -----------                               |  ------------
1    | {YYYY-MM-DD}  |  {Explain the decision that was made here} |  {Name or role}



[Back](./)