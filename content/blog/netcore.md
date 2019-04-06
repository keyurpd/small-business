---
title: "ASP.NET Core"
date: 2016-09-18
draft: false
author: Knight
tags: ["ASP.NET CORE"]
---

Late last year Microsoft released new portable .NET Core 1 and ASP.NET Core 1 frameworks. The idea this time around was to make it really portable after all these years. Unlike Microsoft of the earlier years, this time they made it all open source, and put it on the GitHub. The .NET Core is a subset of .NET Full and is available as a separate installation suitable for variety of operating systems.

> Note: These were known as .NET 5 and ASP.NET 5. Later Microsoft announced to rename them as Core 1 instead.

I have been working on Microsoft technologies for a long time now and I thought this is a good move, as open source is driving more and more innovations. At the same time software world is increasingly talking about PaaS Clouds, Micro-Services, DevOps, and so on.

Hence, I thought of experimenting with it all together with following objectives in mind.

Objectives:

* Try to use free, open-source, and cross-platform stuff as much as possible.
* Create a website in ASP.NET Core targeting .Net Core.
* Run it first on Linux, and then on Docker if possible.
* Host it on the Azure cloud Web App. Leverage built in DevOps of the Azure.
* Connect it to the Azure DocumentDb NoSQL database PaaS.
* Also connect it to the Redis cache PaaS.

Although it seems ambitious at first, everything worked out pretty well at the end!

Sharing the learning from the experiments as follows,

* Visual Studio Code, free and cross-platform, can be used for writing web applications quickly and easily. Atom, Sublime are another good options in the mid-range editors.
* By installing NodeJS, NPM, and using Yeoman scaffolding an empty website template can be created to kick start the development.
* The same can be extended later on to integrate with Grunt, Gulp, and Bower. In fact configuration files for this are also automatically created by scaffolding.
* Once the sample application is ready, it can be hosted on Ubuntu Linux using the built-in web server Kestrel. This was a real challenge as it is based on Libuv, and making it work on Linux along with .NET Core is not straight forward.
* Once it starts running, it is fairly easy to put it on Docker using the official Microsoft ASP.NET image for the Docker container.
* The same can also be hosted on Azure Web App using the built-in Git and DevOps pipeline. It has been all put together very well by Microsoft that provides a seamless experience for the developer.

Once it is running on a PaaS cloud, it can be extended to leverage other PaaS services like NoSQL and Caching for example. In fact, this also works well with one team, one service principle of Micro-Services. All of this combined can finally create a single application ready for the end users.

Since this .NET Core is new, not all libraries are available targeting the new framework. But it is very easy to switch between .NET Core and .NET Full, as Microsoft has come up with a consistent project structure which is based on modern website code conventions.