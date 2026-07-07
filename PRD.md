# ProfileFlow PRD
Version: 1.0  
Status: Draft  
Owner: Founder  
Product Type: Chrome Extension + Native Desktop Helper  
Primary Platform: Chrome Desktop (Windows first)

---

# 1. Product Overview

## Product Name
ProfileFlow

## Tagline
Search any site. Open it in the right account.

## Summary

ProfileFlow is an account-aware URL router and workspace launcher for multi-profile Chrome users.

It allows users to:

- save URLs
- assign URLs to Chrome profiles
- assign accounts to URLs
- group URLs into workspaces
- instantly search and open URLs in the correct Chrome profile

The product solves multi-account workflow friction.

Example:

Search:
ChatGPT

Result:
Open ChatGPT in AI Profile

No manual profile switching.

---

# 2. Core Problem

Users operate:

- multiple Gmail accounts
- multiple Chrome profiles
- multiple SaaS tools
- multiple workspaces

Current browser systems fail because:

Bookmarks store URL only.

Password managers store credentials only.

Session managers store tabs only.

None store:

- URL -> profile mapping
- URL -> account mapping
- URL -> workspace mapping

This creates:

- account confusion
- profile confusion
- wasted time
- context switching

---

# 3. Goals

## Primary Goals

- reduce profile switching friction
- reduce account confusion
- reduce session rebuild time
- provide fast URL search launcher
- provide workspace-based workflows

## Success Criteria

- user launches tool in < 3 seconds
- user finds saved URL in < 2 seconds
- user restores workspace in 1 click

---

# 4. Product Vision

Become the operating layer between:

browser
profiles
accounts
tools
workflows

Users should think:

"I want ChatGPT"

not:

"Which Chrome profile has ChatGPT?"

---

# 5. User Personas

## Persona 1: SEO Specialist

Uses:

ChatGPT
Semrush
Ahrefs
Gmail
Canva
Sheets

Pain:

multiple clients

multiple logins

---

## Persona 2: AI Power User

Uses:

ChatGPT
Claude
Gemini
Perplexity

Pain:

multiple AI accounts

---

## Persona 3: Pinterest Marketer

Uses:

Pinterest
Canva
Tailwind

Pain:

multiple brands

---

## Persona 4: Agency Owner

Uses:

multiple client dashboards

Pain:

client account separation

---

# 6. Product Scope

ProfileFlow consists of:

1. Chrome Extension
2. Native Desktop Helper
3. Local Storage Layer
4. Search Router
5. Workspace Engine

---

# 7. Core Features

# Feature 1: Smart URL Router

Priority: P0

Description:

User searches a saved URL.

System automatically opens it in assigned Chrome profile.

Example:

Input:
chatgpt

System:
Find saved tool

Resolve assigned profile

Launch profile

Open URL

---

## Functional Requirements

- search tools by name
- search tools by URL
- search tools by alias
- fuzzy matching
- instant results
- recent ranking

---

## Acceptance Criteria

Given saved ChatGPT tool

When user searches "chatgpt"

Then system shows ChatGPT

And clicking it launches assigned profile

---

# Feature 2: Workspace Management

Priority: P0

Users can:

- create workspace
- edit workspace
- delete workspace
- archive workspace
- duplicate workspace

---

## Workspace Fields

id

name

assignedProfileId

primaryEmail

description

tags

createdAt

updatedAt

---

# Feature 3: Tool Management

Priority: P0

Users can:

- save tool
- edit tool
- delete tool
- duplicate tool
- move tool

---

## Tool Fields

id

name

url

assignedProfileId

assignedEmail

workspaceId

aliases

notes

tags

launchCount

lastOpened

createdAt

updatedAt

---

# Feature 4: One-click Workspace Launch

Priority: P1

User clicks workspace.

System opens:

all tools

in assigned profile

---

Modes:

Open All

Open Selected

Resume Last Session

---

# Feature 5: Quick Save Current Tab

Priority: P0

Save active browser tab.

Flow:

Click Save

Auto-detect:

title

URL

current profile

User adds:

workspace

email

notes

Save

---

# Feature 6: Alias System

Priority: P1

Users can define aliases.

Examples:

gpt -> chatgpt.com

seo -> semrush.com

pins -> pinterest.com

---

# Feature 7: Domain Rules

Priority: P1

Assign rules:

*.openai.com -> AI Profile

*.pinterest.com -> Pinterest Profile

---

Behavior:

Auto-assign matching URLs.

---

# Feature 8: Favorites

Priority: P1

Pin:

tools

workspaces

---

# Feature 9: Recent Sessions

Priority: P2

Store:

opened tools

workspace state

last session

---

# Feature 10: Import/Export

Priority: P1

Support:

JSON export

JSON import

Backup

Restore

---

# Feature 11: Omnibox Search

Priority: P2

Usage:

pf chatgpt

Open directly.

---

# Feature 12: Keyboard Launcher

Priority: P2

Shortcut:

Ctrl + Shift + K

Open launcher.

---

# 8. User Flows

# Flow A: Save Tool

User opens tool

Click extension

Click Save

Assign:

workspace

email

profile

Save

Done

---

# Flow B: Search Tool

Open extension

Type:

chatgpt

See results

Click Open

System launches assigned profile

Done

---

# Flow C: Launch Workspace

Open extension

Select workspace

Click Launch

System opens all workspace URLs

Done

---

# 9. Architecture

System Architecture:

Chrome Extension
-> Search UI
-> Storage Layer
-> Native Messaging Bridge
-> Native Helper
-> Chrome Launch Engine

---

# 10. Native Helper

Purpose:

Chrome extension cannot directly control other profiles.

Need native helper.

Chrome officially supports Native Messaging for extension-to-native communication.

Reference:
https://developer.chrome.com/docs/extensions/develop/concepts/native-messaging

---

Responsibilities:

receive launch commands

launch Chrome profile

open URL

return status

---

Launch Command:

chrome.exe --profile-directory="Profile 2" https://chatgpt.com

---

# 11. Extension Architecture

Manifest V3

Components:

background service worker

popup UI

options page

storage manager

native messaging client

search engine

---

# 12. Tech Stack

Extension:

React

TypeScript

Manifest V3

Chrome Storage API

Fuse.js (search)

---

Native Helper:

Node.js OR Go

Recommended:

Go

Reason:

single executable

fast

easy install

---

Storage:

chrome.storage.local

Optional:

SQLite in helper

---

# 13. Database Schema

# Workspace

{
"id": string,
"name": string,
"profileId": string,
"primaryEmail": string,
"description": string,
"tags": string[],
"createdAt": number,
"updatedAt": number
}

---

# Tool

{
"id": string,
"name": string,
"url": string,
"profileId": string,
"email": string,
"workspaceId": string,
"aliases": string[],
"notes": string,
"tags": string[],
"launchCount": number,
"lastOpened": number
}

---

# Profile

{
"id": string,
"name": string,
"chromeProfileName": string,
"profilePath": string,
"defaultEmail": string
}

---

# Domain Rule

{
"id": string,
"pattern": string,
"profileId": string
}

---

# 14. Search Engine Requirements

Searchable fields:

tool name

URL

aliases

workspace

email

tags

---

Search behavior:

fuzzy search

instant results

sort by:

relevance

recent usage

launch frequency

---

Performance:

< 100ms

---

# 15. Permissions

Required:

tabs

storage

activeTab

nativeMessaging

contextMenus

omnibox

---

Manifest:

"permissions": [
"tabs",
"storage",
"activeTab",
"nativeMessaging",
"contextMenus"
]

---

# 16. Settings

User-configurable:

Chrome executable path

Profile mappings

Theme

Import/export

Backup

Default profile

---

# 17. Error Handling

Case:

profile not found

Behavior:

show error

---

Case:

URL missing

Behavior:

show invalid URL

---

Case:

native helper missing

Behavior:

show install prompt

---

Case:

launch failure

Behavior:

show retry

---

# 18. Edge Cases

Same site multiple accounts

Expected:

show all matching records

---

Profile deleted externally

Expected:

prompt remap

---

Duplicate URL save

Expected:

warn duplicate

---

Invalid profile path

Expected:

block launch

---

# 19. Security Requirements

Must NOT store:

passwords

cookies

tokens

session data

---

Only store:

URL metadata

email labels

workspace metadata

profile mappings

---

# 20. Performance Requirements

Extension load:

< 300ms

Search:

< 100ms

Launch:

< 1 second

Save tool:

< 200ms

---

# 21. Analytics

Track:

tool launches

workspace launches

search frequency

popular tools

most used workspaces

---

# 22. Monetization

Free:

3 workspaces

50 tools

basic search

---

Pro:

unlimited workspaces

unlimited tools

native launcher

domain rules

analytics

cloud backup

---

# 23. MVP Scope

## MVP v1

Smart URL Router

Tool CRUD

Workspace CRUD

Search

Quick Save

Favorites

Import/Export

---

## MVP v2

Native launcher

Workspace launch

Aliases

Domain rules

---

## MVP v3

Cloud sync

Analytics

Templates

---

# 24. Development Milestones

Week 1:

Extension foundation

Storage models

Tool CRUD

Workspace CRUD

---

Week 2:

Search engine

Quick save

Popup UI

---

Week 3:

Native helper

Native messaging

Launch engine

---

Week 4:

Testing

Bug fixing

Packaging

---

# 25. Testing Plan

Unit tests:

storage

search

routing

---

Integration tests:

extension <-> native helper

launch flow

workspace flow

---

Manual tests:

multi-profile launch

duplicate tool handling

profile switching

---

# 26. Future Features

Team sharing

workspace templates

browser sync

Edge support

Firefox support

mobile companion

AI suggestions

auto-tagging

workspace analytics

---

# 27. Product Positioning

ProfileFlow is not a bookmark manager.

ProfileFlow is a context-aware account launcher.

It remembers:

what to open

where to open

who to open with

---

# 28. Final Definition

ProfileFlow enables users to search any saved website and instantly open it in the correct Chrome profile, with the correct account, in the correct workspace.
