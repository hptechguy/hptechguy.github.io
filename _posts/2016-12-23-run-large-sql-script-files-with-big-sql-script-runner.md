---
layout: post
title: "Run large SQL Script Files with Big SQL Script Runner"
comments: true
description: "Run large SQL Script Files with Big SQL Script Runner"
keywords: "sql, sql server, large sql scripts, large sql script files, t-sql, tsql, ssms, sqlcmd, sql server management studio"
---

Basically, SQL Server Management Studio didn't support us to open large SQL Script Files to run directly. We just can run them within size 300MB. Although Microsoft SQL Team has written a best cmd tool as *sqlcmd*, it doesn't make sure that running on it takes place smoothly. In the past time, I tried using it for a project of my customer and result was unexpected. In the meantime, I gave a thought around my head that I perhaps ought to write a new tool to operate these larger SQL Scripts. Finally, I completed it right away within 2 hours on Sunday. Also, I published to codeplex hub to share it to developer community.

[![big sql script runner cmd](http://download-codeplex.sec.s-msft.com/Download?ProjectName=bigsqlrunner&DownloadId=713696 "Big SQL Script Runner CMD")](http://download-codeplex.sec.s-msft.com/Download?ProjectName=bigsqlrunner&DownloadId=713696)

[![big sql script runner tool](http://download-codeplex.sec.s-msft.com/Download?ProjectName=bigsqlrunner&DownloadId=713703 "Big SQL Script Runner Tool")](http://download-codeplex.sec.s-msft.com/Download?ProjectName=bigsqlrunner&DownloadId=713703)

Hope that you enjoy this utility. More details at: [https://bigsqlrunner.codeplex.com/](https://bigsqlrunner.codeplex.com/) Happy Coding!
