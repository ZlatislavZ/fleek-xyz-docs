---
draft: false
title: Fleek CLI
sidebarCollapsible: false
sidebar_position: 8
date: 2023-01-10T09:00:00.000+00:00
description: Welcome to the documentation for the beta of Fleek.xyz. Whether you are an expert or an absolute beginner, you'll find your answers here.
category: Documentation
keywords: [services, documentation, getting started]
tags:
- Accounts
- Guide
- Learn
- Fleek
---

In this guide, you will find all the information on how to set up and start interacting with Fleek's Command Line Interface (CLI).

### What is a CLI?

A CLI is a command-line program that accepts text input to execute operating system functions. With this, you can interact directly with all the services offered by Fleek directly from your command line. Fleek CLI provides a unified command line interface to Fleek Services.

### Installation

This package requires a minimum of Node.js 16. To install the CLI, run:

```bash copy
npm install -g @fleekxyz/cli
```

### Usage

The Fleek CLI command has the following structure:

```bash copy
$ fleek <service> <command> [options and parameters]
```

To view all available services and commands, you can use:
```bash copy
$ fleek help
```

### Authentication

All the services in the Fleek CLI require authentication. To do this, you have to run:

```bash copy
$ fleek login
```
This will trigger the login process, and we use Web3Auth to manage authentication. Once the flow is completed, you will be greeted like this:

```bash copy
$ fleek login
🔗 Opening browser on https://rough-truth-3196.on.fleek.xyz/login.html?verificationSession=... 
🧑‍💻 Please login to continue
✅ Successfully logged in.
```

If at any point you want to log out, you can do so:

```bash copy
$ fleek logout
✅ Successfully logged out.
```

### Projects

As explained [here](./projects), to interact with services, you need to have a project. This can be created and managed via the CLI too!

To create a project, you can do it like this:

```bash copy
$ fleek projects create
$ ? Enter project name: › 
```

When you enter a correct name, you will be automatically switched to it. Additionally, you can switch between different projects using the 'switch' command, which will prompt a selector:

```bash copy
$ fleek projects switch
❯   project-1
    project-2
    project-3
```
