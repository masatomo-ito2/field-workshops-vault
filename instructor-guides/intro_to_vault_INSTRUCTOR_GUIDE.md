# Introduction to Vault - Instructor Guide

This guide will prepare you to deliver a half-day [Introduction to Vault Workshop](https://hashicorp.github.io/field-workshops-vault/slides/multi-cloud/vault-oss). This workshop content is suitable for HashiCorp community members, prospects and customers. The workshop is a combination of lecture slides and hands-on Instruqt labs that introduce new users to some of Vault's features. This workshop focuses on open-source features and is targeted toward new users. The workshop may be presented in-person, over the web, or as a self-guided tutorial.

The workshop alternates between lectures with accompanying slides and hands-on lab exercises. New concepts that are introduced in the slides are reinforced in the labs. Participants will learn both the theory and practice of Vault. As an instructor you should be well familiar with the slide deck and the Instruqt tracks used in the workshop. Go through the course and make sure you understand all of the major concepts and lab exercises.

When possible you should attend a live training session to observe and learn from another instructor. We will also have video recordings of this workshop available soon.

### Prerequisites
Prerequisites are minimal. All that is required to participate in the workshop is a web browser and Internet access. No software needs to be downloaded or installed. Self-contained lab environments run on the [Instruqt](https://play.instruqt.com/hashicorp) platform, and markdown-based slide decks are published as Github Pages websites.

The Instruqt tracks include terminal tabs that can be used to execute Vault CLI commands. They also include the Vault UI.

All instructors and TAs from HashiCorp should be sure to register themselves with Instruqt and then post a message in our Slack channel, #proj-instruqt, asking to be added to the HashiCorp organization within Instruqt. This is important even if the tracks are public since only members of the HashiCorp organization can see the useful "Skip to Challenge" button on challenges of tracks within this organization.

### Email Invitation
Here is some boilerplate text you can use or customize when inviting or announcing your workshop:

```
Introduction to Vault
A hands-on technical workshop

Learn how to configure Vault clusters and manage secrets in them. Vault is an API-driven, cloud-agnostic secrets management solution. Vault is easy for beginners and powerful for experts. Join us for a half-day training that will get you up and running quickly with Vault.

Topics covered in the workshop include:

* Vault Overview
* Interacting with Vault
* Running a Production Server
* Vault Secrets Engines
* Vault Authentication Methods
* Vault Policies
* Dynamic Database Secrets
* Encryption as a Service

A modified version of this workshop also covers Vault's AWS secrets engine and authentication method.

The only prerequisites for this workshop are a web browser and willingness to learn.
```

### Markdown Slide Deck
The slide deck for this training is published here:

#### https://hashicorp.github.io/field-workshops-vault/slides/multi-cloud/vault-oss

The optional extension for AWS are here:
#### https://hashicorp.github.io/field-workshops-vault/slides/aws/vault-oss

#### Navigation
Use the arrow keys (up/down or left/right) to navigate back and forth between slides.

Press the `P` key to enter presenter mode and reveal the speaker notes.

Press the `C` key to pop open an external window that will stay synced with your speaker notes window. This is useful for keeping notes on your laptop while showing the presentation on the projector.

#### RemarkJS
The slide deck for this training is written completely in [Markdown](https://guides.github.com/features/mastering-markdown/) using the [RemarkJS](https://remarkjs.com/#1) framework. This allows us to publish slide decks from a source code repository. The slide deck is easy to maintain, lightweight, and can be accessed from anywhere. Updates and changes to the deck can be made quickly and efficiently by simply editing the markdown source files. If you find any mistakes or issues with the slides please add them to our issue tracker:

https://github.com/hashicorp/field-workshops-vault/issues

### Hands-on Labs
At certain points in the slide deck there are links to the lab exercises. [Instruqt](https://instruqt.com/hashicorp) is our lab platform. While all of the Vault workshop tracks are actually public, the slides use links to permanent Instruqt invitations that require users to register with Instruqt. We do this so that HashiCorp Field Marketing can collect the emails of users who start tracks during public or private workshops or on their own after following the links from the slides.

Participants can register with Instruqt [here](https://play.instruqt.com/signup?from=/public). Instruqt supports registering with an email and via Google, GitHub, and Twitter.

Students may have questions during the labs. When presenting a workshop be sure to give enough time for all your participants to go through the labs. Remember that this is probably their first time using a tool like Vault.

As mentioned in the Prerequisites section, all HashiCorp instructors and TAs for workshops should register with Instruqt and then post a message in our Slack channel, #proj-instruqt, asking to be added to the HashiCorp organization in Instruqt.

Members of the HashiCorp organization in Instruqt can hover over any challenge in any track in that organization and see a "Skip to Challenge" button. After starting a track, you can use these buttons to run the track's setup and solve scripts up to the challenge you want to skip to. When skipping to a challenge, always be sure to click the "Normal Skip" button too.

https://play.instruqt.com/hashicorp/tracks/vault-basics

Go through this track start to finish and make sure you understand all the challenges. This track covers the Vault CLI and UI, running a dev Vault server and writing a secret to it, using the Vault HTTP API, running a production Vault server, using the KVv2 secrets engine and the Userpass auth method, and Vault policies.

https://play.instruqt.com/hashicorp/tracks/vault-dynamic-database-credentials

Go through this track start to finish and make sure you understand all the challenges. This track covers Vault's database secrets engine.

https://play.instruqt.com/hashicorp/tracks/vault-encryption-as-a-service

Go through this track start to finish and make sure you understand all the challenges. This track covers Vault's encryption as a service capabilities as implemented in its Transit secrets engine.

The following two tracks are optional tracks for use with customers focused on AWS:

https://play.instruqt.com/hashicorp/tracks/vault-aws-dynamic-secrets

Go through this track start to finish and make sure you understand all the challenges. This track covers Vault's AWS secrets engine.

https://play.instruqt.com/hashicorp/tracks/vault-aws-auth-method

Go through this track start to finish and make sure you understand all the challenges. This track covers Vault's AWS auth method.

### Timing
The following schedule assumes you have a group of participants who are brand new to Vault. You should budget about four hours for this workshop including a short break. This is meant as a guideline, you can adjust as needed. If you prefer to alternate the slides of the "Interacting with Vault" chapter with the first 3 challenges of the "Vault Basics" track, you can do that.

If you want to cover the optional AWS slides and Instruqt tracks, add 1 hour.

0:00 - 0:10 - Wait for attendees, make introductions<br>
0:10 - 0:25 - Vault Overview<br>
0:25 - 0:40 - Interacting with Vault<br>
0:40 - 1:00 - Lab: Vault Basics: Challenges 1-3<br>
1:00 - 1:10 - Running a Production Vault Server<br>
1:10 - 1:20 - Lab: Vault Basics: Challenge 4<br>
1:20 - 1:30 - Vault Secrets Engines<br>
1:30 - 1:40 - Lab: Vault Basics: Challenge 5<br>
1:40 - 1:50 - Vault Authentication Methods<br>
1:50 - 2:00 - Lab: Vault Basics: Challenge 6<br>
2:00 - 2:10 - Break<br>
2:10 - 2:20 - Vault Policies<br>
2:20 - 2:35 - Lab: Vault Basics: Challenge 7<br>
2:35 - 2:50 - Dynamic Database Secrets<br>
2:50 - 3:20 - Lab: Vault Dynamic Database Credentials<br>
3:20 - 3:35 - Encryption as a Service<br>
3:35 - 4:05 - Lab: Vault Encryption as a Service<br>
4:05 - 4:15 - Wrap-up<br>
