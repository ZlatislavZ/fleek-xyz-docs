---
draft: false
title: Storage
sidebarCollapsible: false
sidebar_position: 2
date: 2023-01-10T09:00:00.000+00:00
description: Welcome to the documentation for the beta of Fleek.xyz. Whether you are an expert or an absolute beginner, you'll find your answers here..
category: Documentation
keywords: [services, documentation, getting started]
tags:
- Edge Platform
- CDN
- Guide
- Learn
- Fleek
---

### Introduction

In Fleek we offer a storage service that you can use to store your files in a decentralized way. We support the following protocols:

- IPFS
- Arweave
- Filecoin

To guarantee the best performance and availability we use a combination of these protocols. We use IPFS as the main storage protocol and we use Arweave and Filecoin as a backup layer. This allows us to provide a high availability and performance service. By default we are using Filecoin as the backup layer but all the configuration can be changed in the storage settings.

Storage is a service unique for every project. This means that you can have different storage configurations for each project you have in Fleek.

### Add a File or Directory

To add a file to your storage you first need to navigate to the `Files` section in your project dashboard and click on the `Upload File` button. This will open a modal where you can select one or multiple files to upload.

This will be uploaded to IPFS and in the background it will be uploading to Filecoin and/or Arweave depending on your configuration.

To add a directory simply select  the `Upload Directory` button and select the directory you want to upload.

### Accessing a file or directory

To access a file or directory you can click on the three dots icon in the file or directory row and select the `Copy URL` option. This will copy the URL to your clipboard and you can use it to access the file or directory. By default Fleek will be using Public gateways to surface the content. If you want you can set up a custom domain to access the content that will allow you to have a more performant a branded experience.

To do this you can follow the steps in the [Gateways](/docs/gateways) section.

### Deleting a file or directory

To delete a file or directory you can click on the three dots icon in the file or directory row and select the `Delete` option. This will remove the file or directory from your storage. This action is irreversible.


### Content Addressing

In Fleek, all files in storage are made content-addressable by using IPFS as the addressability layer, which means all files stored on Fleek are stored on IPFS by default aside from the decentralized-storage layer of choice (Filecoin/Arweave). Each file will receive its unique immutable IPFS content hash to make it addressable under a common denominator/format that is standard in web3.

- IPFS hashes look like: `QmX4XRaPP6jBSDiYr3tK7fEBWSA5QURS8WZ87ZvPRJgAqK`

And they can be accessed via either Fleek's gateways, or a public gateways such as `ipfs.io/ipfs/<yourhash>`. While immutable, you can use IPNS to map dynamically changing IPFS hashes to a static hash/record (IPNS). See our CLI/SDK section for instructions on how to manage IPNS records.