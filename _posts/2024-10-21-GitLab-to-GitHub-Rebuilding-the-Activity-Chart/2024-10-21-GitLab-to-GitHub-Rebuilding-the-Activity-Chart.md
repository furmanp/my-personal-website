---
layout: post
title: "GitLab to Github: Rebuild Your Activity Chart Effortlessly"
date: 2024-10-21 21:00:00 +0000
categories: [general]
tag: [ web, software, go ]
---

# motivation

About a month ago, I started a new position, and my current company uses GitLab to manage its codebase. However, I
wanted to reflect this activity on my GitHub profile, which remains the go-to platform for collaborations and a key
point of interest for recruiters evaluating a developer’s work.

I began searching for a tool that could import my GitLab activity into my GitHub profile, but none of the available
options fully met my expectations. This gave me the perfect opportunity to explore two goals I had in mind: syncing my
GitLab contributions with GitHub and learning the Go programming language. So, I decided to build my own tool to
accomplish this.

I had two primary requirements:

	1.	Keep my activity consistently up to date.
	2.	Automate the process to avoid manual effort.

# solution

## first step: making it work

To start, I focused on developing a manual process. Fortunately, both GitLab and GitHub provide extensive APIs with
thorough documentation, which simplified the development process. Here’s the approach I took:

	1.	Retrieve GitLab User ID: Identify the user whose activity will be imported.
	2.	Fetch User Contributions: Gather all contributions (commits, comments, pull requests) from the projects the user is involved in.
	3.	Extract Commits: For each project, retrieve the user’s commits.
	4.	Recreate Commit Activity: Mirror the commit activity in a new GitHub repository.
	5.	Publish to GitHub: Push the recreated commits to a GitHub repository.

Each commit contains the essential information—message, SHA (hash), author, and timestamp—allowing me to replicate the
activity chart on GitHub accurately. However, one key challenge I encountered was preventing duplicate commits. Since
the SHA (commit hash) is unique and generated at the time of commit, I decided to include the original GitLab commit SHA
in the GitHub commit messages. This allowed me to filter out already-imported commits, ensuring the process stayed
accurate without creating duplicates.

Additionally, I made sure that only the commit history was replicated without any actual code, eliminating any risk of
violating company policies by copying proprietary code to GitHub.

## automating the process

Once I got the manual process working, my next goal was to automate it. This required setting up a system that would
periodically fetch and push the imported commits to the GitHub repository without any manual intervention.

To achieve this, I needed to:

    1.	Set Up a Remote Repository: Point my tool to the correct GitHub repository where the activity would be mirrored.
    2.	Use GitHub Personal Access Token: Authenticate the push operation using a personal access token (PAT) to allow the script to push updates to the repository’s worktree.

With these changes in place, the tool now automatically updates my GitHub profile with the activity from GitLab,
ensuring that my contributions stay up to date without requiring manual effort.

To take it a step further, I decided to set up a CI/CD pipeline that runs the tool on a schedule. Using GitHub Actions,
I can keep my GitHub profile updated automatically. This setup is also easy for others to use: they can simply fork the
repository, set the environment variables, and start importing their GitLab commit history with minimal effort.

With the CI/CD pipeline in place, the entire process of syncing my GitLab activity to GitHub is fully automated. The
workflow runs daily (or at any defined interval), fetches the latest contributions from GitLab, and syncs them with my
GitHub profile without any manual intervention.

I’m pleased that this simple tool has completely taken a simple task off my mind. Maybe in the future,
I’ll expand it to support other platforms as well. Also, feel free to contribute or create an issue if you like.
For anyone interested in the tool, you can find it
here: <a href="https://github.com/furmanp/gitlab-activity-importer" target="_blank" rel="noopener">link to
repository.</a>
