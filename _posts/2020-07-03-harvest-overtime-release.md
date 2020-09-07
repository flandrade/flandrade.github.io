---
layout: post
date: 2020-07-03 21:55:00
title: Announcing harvest-overtime ⏰
summary:
  Command-line interface to calculate employee's overtime with Harvest's CSV reports. This tool
  provides the information to calculate overtime pay correctly.
categories: projects
tags: [english, cli, project, harvest, typescript]
---

[Harvest](https://www.getharvest.com/) is a service that provides time tracking for small
businesses. They provide numerous reports to make sure projects are healthy. However, although you
can keep track of employees' working time, there is no visibility of overtime details.

For this reason, I'm happy to announce
[harvest-overtime](https://github.com/flandrade/harvest-overtime). It's a command-line interface to
calculate employee's overtime with
[Harvest's CSV reports](https://help.getharvest.com/harvest/reports/managing-harvest-reports/time-report/).
The goal of this tool is to provide the information to calculate overtime pay correctly.

### Features ✨

- Calculates overtime: generates a report or prints to the command line.
- Includes total time per day and an overtime report of both weekdays and weekends.
- Supports any reporting period. It can be a week or several months.
- Supports standard full-time work (40 hours per week: 8 hours per day), but you can change this
  value.

### Usage and Feedback 🏗

To use this tool, please
[check the documentation](https://github.com/flandrade/harvest-overtime#harvest-overtime-). You'll
find an [installation guide](https://github.com/flandrade/harvest-overtime#harvest-overtime-) and
[some examples](https://github.com/flandrade/harvest-overtime#-examples). This is how a final report
looks like:

<script src="https://gist.github.com/flandrade/b1121bba11ae01c97ac8859bf1673f81.js"></script>

This CLI was built with TypeScript and Node.js. If you have any suggestions or want to let me know
what you think of this tool, feel free to open
[an issue](https://github.com/flandrade/harvest-overtime/issues).
