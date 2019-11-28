# [liachskeleton](https://liachmodded.github.io/liachskeleton/overview-summary.html)

## Overview

A java gradle template by [liachmodded](https://github.com/liachmodded).

Replace the readme with whatever you want!

[Source](https://github.com/liachmodded/liachskeleton/)

## Usage
- Change:
  - references in gradle.properties
  - the repo name in .travis.yml
  - change installed data generators
  - The license (default is MPL-2.0)
    - `codeLicense` in gradle.properties, need to be one that bintray accepts, e.g. `Unlicense`
    - change header
- For travis ci:
  - Add environmental variables:
    - `GITHUB_OAUTH_TOKEN`: a github access token that can push to this repo (for javadoc page and releasing) and to publish GitHub packages
    - `bintray_user`: the username of the bintray account that publishes stuff to bintray (for maven)
    - `bintray_key`: the access token for that bintray account

## Features
- Auto license enforcement with licenser
- Auto publication of javadocs and releases to GitHub
  - Requires a GitHub OAUTH token
  - GitHub page may not show up on initial deployment, set GitHub page to build from a different source (e.g. master branch) and set it back to gh-pages branch to enlighten GitHub
- Auto publication of playable mod to GitHub Package Registry
  - Requires a GitHub OAUTH token
- Auto publication of artifacts to free, reliable maven (bintray; much better than jitpack, which stalls your gradle)
  - You need to link a GitHub account to bintray and obtain an api key
  - Maven repo is at `https://dl.bintray.com/${repoOwner}/${bintrayRepo}`
