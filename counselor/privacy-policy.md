---
layout: default
title: Privacy Policy — counselor
---

# Privacy Policy — counselor

**Last updated:** 11 September 2026

counselor is a private, self-hosted Discord bot operated by an individual for
personal use in a single channel. It is not a commercial service, it is not
offered to the public, and it has no users other than the members of the one
channel it is configured to read.

This policy describes exactly what it does with what it reads.

## What it reads

In the **one Discord channel it is configured for**, and nowhere else, counselor
receives every message posted and stores:

- the message text
- the author's Discord display name and numeric user ID
- the timestamp
- whether the author was a bot

It does not read direct messages, other channels, other servers, voice, or
attachments. It has no access to anything outside the single configured channel.

## Where it is stored

In one SQLite file on a machine owned and physically controlled by the operator,
on a private home network. It is not stored on any cloud service, and the file
is not reachable from the public internet.

The operator has filesystem access to that machine and can therefore read the
database. No one else has access.

## How long it is kept

| Data | Retention |
|---|---|
| Raw message text | **30 days**, then automatically deleted |
| Distilled notes (recurring patterns, stated needs, agreements, appreciations) | Until manually erased |
| Record of when the bot spoke | Until manually erased |

The raw transcript expires deliberately. What survives is a short summary of
what was learned, not the conversation itself.

`/counselor forget` erases everything immediately — raw messages, notes, and
history — with no recovery.

## What is sent to a third party

**This is the most important section.**

To generate a response, counselor sends recent message text from the channel to
a third-party large language model provider over the internet. As configured,
that provider is **Moonshot AI (Kimi)**, at `api.moonshot.ai`.

This means the content of messages in the channel leaves the operator's machine
and is processed on infrastructure controlled by that provider, subject to that
provider's own privacy policy and data-handling practices, and potentially in a
different legal jurisdiction.

What is sent: recent message text, participants' display names, and any stored
notes relevant to the moment. What is not sent: anything from outside the
channel.

The provider is configurable. Pointing counselor at a model running locally
would mean no message content ever leaves the machine. That is a one-line
configuration change, and the choice of provider is the single largest privacy
decision in this system.

## Backups

The database is backed up daily to a network-attached storage device on the same
private home network. These backups are deliberately **excluded** from the
offsite/cloud backup process that covers other systems — this data does not
leave the premises. Backups inherit the same retention as the live database.

## What it is never used for

The data is not sold, rented, shared, published, or used to train any model. It
is not combined with data from any other source. There is no analytics,
telemetry, advertising, or third-party tracking of any kind, beyond the model
provider call described above.

## Controls

| Command | Effect |
|---|---|
| `/counselor status` | Shows everything currently held |
| `/counselor forget` | Permanently erases everything |
| `/counselor pause` | Stops it speaking for a set period |
| `/counselor resume` | Reactivates it |

Removing the bot from the channel stops all collection immediately. Deleting the
database file destroys everything it holds.

## Legal status

counselor is not a healthcare provider, not a covered entity, and this data is
not a medical record. It is not protected by HIPAA, therapist–patient privilege,
or any equivalent confidentiality protection. It is a personal note-keeping and
reflection tool, and its contents would have the same legal status as any other
private file on a personal computer.

## Children

Not intended for and not to be used by anyone under 18.

## Changes

Material changes will be reflected in this document with an updated date. Since
this is a private tool with two users, changes are communicated directly.

## Contact

Through the operator of the Discord server in which the bot runs.
