---
title: C# - Paths to system folders
date: 2016-01-29 20:22:36
tags: daily, learn
---

##**GIT - Branches, Tags and Commits**

I was concern what will happend with my comments in the case i remove a branch.

In git Commits are independents of branch's and Tag's. This last two are just pointers to certain commit. Trying to delete a Branch could create unreachable commits but if this are tag they become reachable.

Removing branches will not remove commits, they will just become unreachable. Unless they are deleted with the git-gc command for example.
