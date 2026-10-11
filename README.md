# intro
Theres alot of stuff to this since I already am on the fucking v4.5.6 version of this tool
but you can do pretty much anything with this tool and its very powerful 
even more powerful than devtools itself cause it has a front and back-end to it
and yes the back-end is an external but if you want you can add api's

showcase on my yt
https://www.youtube.com/@backdevsinister

**I made this tool for educational purposes only and anyone abusing this tool its not my problem. >///<**
also join my discord: https://discord.gg/3qxSjJVct
# How to use FULL TUTORIAL
**Current Version:** 4.5.6  
**Platform:** Google Chrome / Chromium-based browsers  
**Extension:** Manifest V3  
**Optional Backend:** Node.js

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [First Launch](#first-launch)
- [Dashboard](#dashboard)
- [Sources](#sources)
- [Live Edit](#live-edit)
- [Network](#network)
- [Saved XHRs](#saved-xhrs)
- [Network Overrides](#network-overrides)
- [Storage](#storage)
- [Cookies](#cookies)
- [Console](#console)
- [CSS](#css)
- [JSON](#json)
- [Tools](#tools)
- [Server](#server)
- [API Connections](#api-connections)
- [Cloud](#cloud)
- [Settings](#settings)
- [Backend Settings](#backend-settings)
- [Troubleshooting](#troubleshooting)
- [Security](#security)
- [Project Structure](#project-structure)
- [Development](#development)
- [Architecture](#architecture)

---

## Overview

RichAF is a custom Chrome DevTools workspace designed for inspecting, editing, testing, and debugging websites. (and maybe changing them)

It combines several development tools into a single uhh place?:

- Page inspection
- Sources explorer
- HTML editing
- CSS editing
- JavaScript console
- Network inspection
- XHR/FETCH replay
- Request overrides
- LocalStorage editor
- SessionStorage editor
- Cookie editor
- JSON utilities
- API connection management
- Persistent Cloud workspace
- Local backend
- Custom backgrounds
- Backend configuration

RichAF can operate without the backend for most browser-side features.

The optional backend adds persistent storage and server-side features.

---

## Features

| Feature | Backend Required |
|---|---|
| Dashboard | No |
| Sources | No |
| Live Edit | No |
| Network | No |
| Saved XHRs | No |
| Network Overrides | No |
| LocalStorage | No |
| SessionStorage | No |
| Cookies | No |
| Console | No |
| CSS | No |
| JSON | No |
| Tools | No |
| Custom UI Settings | No |
| Cloud | Yes |
| API Connections | Yes |
| Backend Settings | Yes |
| Server Events | Yes |
| Background Uploads | Yes |

---

# Installation

## Requirements

You will need:

- Google Chrome
- Node.js 18+ if using the backend
- npm if using the backend

---

## Installing the Extension

Open:

    chrome://extensions

Enable:

    Developer mode

Click:

    Load unpacked

Select the extracted RichAF extension directory.

Your folder should look similar to:

    RichAF-extension/
    ├── backend/
    ├── icons/
    ├── devtools.html
    ├── devtools.js
    ├── manifest.json
    ├── panel.html
    ├── panel.js
    ├── panel.css
    ├── package.json
    └── start-server.bat

---

# Opening RichAF

Open any website you want to inspect.

Open Chrome DevTools:

    Right Click → Inspect

Then select:

    RichAF

RichAF will open inside Chrome DevTools.

---

# First Launch

On first launch, RichAF may display its startup/profile screen.

The default development profile included in the current build is:

    Username: Admin
    Password: admin123

After authentication, RichAF remembers the authenticated state locally.

> For a public/custom build, change the default credentials.

---

# Navigation

RichAF contains the following main sections:

    Dashboard
    Sources
    Live Edit
    Network
    Storage
    Console
    CSS
    JSON
    Tools
    Server
    Cloud
    Settings

Each section has a different purpose.

---

# Dashboard

The Dashboard provides an overview of the currently inspected page.

Depending on the page, it can display information such as:

    Page URL
    Page title
    DOM statistics
    Scripts
    Stylesheets
    Links
    Images
    Iframes
    Resources

---

## Refreshing the Dashboard

Use:

    Refresh

to update the information.

---

## Reloading the Page

Use:

    Reload

to reload the inspected website.

---

## Hard Reload

Use:

    Hard Reload

when you need to force the page to reload its resources.

---

## Inspect Body

Use:

    Inspect Body

to quickly target the page's <body> element.

---

## Copy URL

Use:

    Copy URL

to copy the current page URL.

---

# Sources

The Sources tab provides a DevTools-style resource explorer.

Example:

    Page

    └── example.com
        ├── assets
        │   ├── app.js
        │   ├── style.css
        │   └── index.html
        ├── images
        │   └── logo.png
        └── fonts

Click a file to open it in the source editor.

---

## Supported Resource Types

RichAF can recognize resources such as:

    HTML
    CSS
    SCSS
    SASS
    JavaScript
    TypeScript
    JSON
    Images
    Fonts

---

## Source Tabs

When multiple resources are opened, RichAF creates tabs.

Example:

    index.html
    app.js
    style.css

Click a tab to switch between resources.

---

## Source Tools

The source editor provides tools such as:

    Copy
    Download
    Wrap
    Refresh

---

## SCSS and SASS

RichAF can recognize SCSS and SASS resources when they are exposed to the browser.

However, many websites compile SCSS/SASS before sending the final CSS to the browser.

For example:

    styles.scss
        ↓
    Sass compiler
        ↓
    styles.css
        ↓
    Browser

In that situation, the browser normally only exposes:

    styles.css

RichAF cannot recover source files that were never sent to the browser.

---

# Live Edit

Live Edit allows you to modify elements on the currently inspected page.

RichAF uses Chrome DevTools' selected element context.

The selected element is commonly available as:

    $0

---

## Loading the Selected Element

First select an element in DevTools.

Then open:

    RichAF → Live Edit

Click:

    Load $0

RichAF will load the currently selected element.

---

## Editing Text

Use:

    Text Content

Enter the new text and click:

    Apply Text

Example:

    Original:
    <h1>Hello</h1>

    New:
    <h1>Hello RichAF</h1>

The change is applied to the live page.

---

## Editing Attributes

You can view and modify attributes.

Example:

    <img
        src="image.png"
        class="avatar"
        disabled
    >

You can modify:

    src
    class
    disabled

or add custom attributes such as:

    data-debug="true"

---

## Adding an Attribute

Click:

    Add Attribute

Enter:

    Name:
    data-debug

    Value:
    true

Then apply the change.

---

## Editing Inline Styles

You can modify inline CSS.

Example:

    color: red;
    font-size: 20px;
    display: block;

Click:

    Apply Styles

to apply the changes.

---

## Hide an Element

Use:

    Hide

to temporarily hide the selected element.

---

## Show an Element

Use:

    Show

to restore the element's visibility.

---

## Outline

Use:

    Outline

to visually highlight the selected element.

---

## Delete Element

Use:

    Delete

to remove the selected element from the current page.

This is normally temporary.

Reloading the page will generally restore the original page.

---

# Network

The Network tab allows you to inspect requests made by the inspected website.

Common filters include:

    All
    XHR
    Fetch
    Document
    JavaScript
    CSS
    Images
    Other

---

## Searching Requests

Use the Network search/filter field.

For example:

    /api/

This can help locate requests such as:

    /api/users
    /api/profile
    /api/items

---

## Request Details

Click a request to view its information.

Depending on the request, RichAF can display:

    General
    Request Headers
    Response Headers
    Payload
    Response
    Timing

---

## General

General information can include:

    Method
    URL
    Status

---

## Request Headers

Request headers may include:

    Content-Type
    Accept
    Authorization
    User-Agent

---

## Response Headers

Response headers may include:

    Content-Type
    Cache-Control
    Content-Length

---

## Payload

The Payload section shows information sent with the request.

Example:

    {
      "username": "example",
      "enabled": true
    }

---

## Response

The Response section shows the server response.

JSON responses can be formatted for easier reading.

---

# Saved XHRs

RichAF allows you to save XHR/FETCH requests.

Saved requests persist through RichAF reloads and page reloads.

---

## Creating a Saved XHR

Open:

    Network

Click:

    New XHR

Enter:

    Method
    URL
    Headers
    Body

Example:

    Method:
    POST

    URL:
    https://example.com/api/test

Headers:

    Content-Type: application/json

Body:

    {
      "hello": "world"
    }

Click:

    Save XHR

---

## Editing a Saved XHR

Select a saved request.

Click:

    Load

or:

    Edit

Modify the request.

Then click:

    Update Saved

---

## Deleting a Saved XHR

Select the request.

Click:

    Delete

---

## Replaying a Request

Load a saved request and use:

    Replay

RichAF will send the request and display the result.

---

## Copy Fetch

Use:

    Copy Fetch

to generate a JavaScript fetch representation.

Example:

    fetch("https://example.com/api/test", {
      method: "POST",
      headers: {
        "Content-Type": "application/json"
      },
      body: JSON.stringify({
        hello: "world"
      })
    });

---

## Copy cURL

Use:

    Copy cURL

to generate a command-line representation of the request.

---

# Network Overrides

RichAF includes a Fetch/XHR override engine.

Overrides can be used for development and testing.

Supported modes include:

    Block
    Mock
    Force

---

## URL Matching

Specify a URL or URL fragment.

Example:

    /api/user

Requests matching that URL can be intercepted.

---

## Method Matching

You can restrict an override to a method such as:

    GET
    POST
    PUT
    PATCH
    DELETE

---

## Mock Response

Mock responses allow you to substitute a response with custom data.

Example:

    {
      "username": "TestUser",
      "premium": true
    }

You can specify:

    Status
    Response Headers
    Response Body

---

## Force Response

Force a particular response for matching requests.

This is useful for testing frontend behavior against different server responses.

---

## Block Request

Block a matching request entirely.

For example:

    /api/analytics

can be blocked while testing a website locally.

---

## Request Delay

You can add an artificial delay.

Example:

    Delay:
    2000

This simulates a slow response.

Useful for testing:

    Loading states
    Spinners
    Skeleton screens
    Timeout handling
    Error handling

---

## Installing an Override

Configure the rule.

Then click:

    Install Fetch Override

The override becomes active.

---

## Removing an Override

Click:

    Remove Override

RichAF restores the original Fetch/XHR behavior.

---

## Copying an Override

Use:

    Copy Rule JSON

to copy the override configuration.

---

# Storage

RichAF provides browser storage management.

Supported storage types include:

    LocalStorage
    SessionStorage

---

# LocalStorage

Select:

    Local

RichAF displays the current localStorage entries.

---

## Editing LocalStorage

Select an entry.

Change its value.

Click:

    Set

---

## Adding LocalStorage

Use:

    Add

Enter:

    Key
    Value

Then save it.

---

## Clearing LocalStorage

Use:

    Clear

to remove the stored entries.

> Be careful when clearing storage because websites may rely on it for their current state.

---

# SessionStorage

Select:

    Session

to inspect sessionStorage.

You can:

    View
    Add
    Edit
    Delete
    Clear

sessionStorage entries.

---

# Cookies

RichAF provides a cookie editor through Chrome's cookie APIs.

Cookies are associated with the inspected website.

---

## Viewing Cookies

Open:

    Storage

Find:

    Cookies

Click:

    Refresh

---

## Cookie Fields

RichAF supports fields such as:

    Name
    Value
    Domain
    Path
    SameSite
    Secure
    HttpOnly

---

## Adding a Cookie

Click:

    New

Enter the cookie information.

Then:

    Save Cookie

---

## Editing a Cookie

Select a cookie.

Click:

    Edit

Change its information and save.

---

## Deleting a Cookie

Select a cookie.

Click:

    Delete

---

## Cookie Security

Browser cookies remain in Chrome's browser context.

They are not automatically uploaded to the RichAF backend.

The RichAF backend is intended for RichAF's own persistent data.

---

# Console

RichAF includes a JavaScript console for the inspected page.

Example:

    document.title

Another example:

    document.querySelectorAll("img").length

JavaScript executed through this interface runs in the context of the inspected page.

---

# CSS

The CSS tab provides tools for testing CSS against the current page.

Typical workflow:

    Write CSS
        ↓
    Apply
        ↓
    Inspect result
        ↓
    Modify CSS
        ↓
    Apply again

These changes are generally live-page changes rather than permanent website changes.

---

# JSON

RichAF provides JSON utilities.

Common operations include:

    Format
    Minify
    Copy

---

## Format JSON

Input:

    {"user":{"name":"Alex","active":true}}

Output:

    {
      "user": {
        "name": "Alex",
        "active": true
      }
    }

---

## Minify JSON

Converts formatted JSON into compact JSON.

Example:

    {
      "hello": "world"
    }

becomes:

    {"hello":"world"}

---

## Copy JSON

Copies the processed JSON to the clipboard.

---

# Tools

The Tools section provides miscellaneous developer utilities.

Depending on the current build, these include functionality around:

    Page inspection
    HTML capture
    Resource URLs
    Console operations
    Backend events
    Developer testing

---

# Server

The Server tab connects RichAF to the optional local backend.

Default backend address:

    http://127.0.0.1:3210

---

# Why Use the Backend?

The extension can perform many browser-side tasks without a backend.

The backend adds persistent functionality such as:

    Cloud
    API Connections
    Backend Settings
    Server Events
    Projects
    Background Storage
    Persistent Configuration

---

# Installing the Backend

Install Node.js.

Official website:

    https://nodejs.org/

Then open a terminal in:

    RichAF-extension/backend

Run:

    npm install

Then:

    npm start

You should see something similar to:

    RichAF backend listening on http://127.0.0.1:3210

---

# Windows Quick Start

RichAF includes:

    start-server.bat

You can double-click the batch file to start the backend.

---

# Connecting to the Backend

Open:

    RichAF → Server

Enter:

    http://127.0.0.1:3210

Click:

    Connect

---

# Ping

Click:

    Ping

to test whether the backend is responding.

---

# Backend Connection Detection

RichAF periodically checks the backend.

It can detect states such as:

    Online
    Offline
    WebSocket Disconnected

If the Node.js process is closed while RichAF is open, RichAF can detect that the backend is no longer available.

---

# WebSocket

RichAF uses WebSockets for real-time backend communication.

Default WebSocket endpoint:

    ws://127.0.0.1:3210/ws

---

# Server Initialization

If the backend has not created its required storage directories, use:

    Initialize Server

This prepares the backend's local data storage.

---

# API Connections

API Connections allow you to save and test external API endpoints.

> RichAF 4.5.6's API Connections feature is primarily a connection manager/tester. It is not yet a full Postman-style API request workspace.

---

## Creating an API Connection

Open:

    Server

Find:

    API Connections

Click:

    Add API

Enter:

    Name
    Base URL
    Authentication

---

## Example

Name:

    Example API

Base URL:

    https://api.example.com

Authentication:

    None

Click:

    Save

---

# API Authentication

RichAF supports:

    None
    Bearer
    API Key

---

## No Authentication

Choose:

    None

Use this for APIs that do not require credentials.

---

## Bearer Authentication

Choose:

    Bearer

Provide the token.

RichAF uses:

    Authorization: Bearer YOUR_TOKEN

---

## API Key Authentication

Choose:

    API Key

Provide the key/header information.

A common format is:

    X-API-Key: YOUR_KEY

---

# Testing an API

Select the saved API connection.

Click:

    Test

RichAF will test the connection.

The result can include:

    HTTP Status
    Response Time
    Response Preview

Example:

    200 OK
    143 ms

    {
      "status": "ok"
    }

---

# Deleting an API Connection

Select the API.

Click:

    Delete

---

# API Security

Do not treat RichAF's API connection storage as a production secrets manager.

Avoid storing sensitive production credentials such as:

    Production passwords
    Private signing keys
    Database credentials
    Master API keys

in an unsecured local development environment.

---

# Cloud

Cloud is RichAF's persistent workspace.

It requires the backend.

The current Cloud system stores files locally through the RichAF backend.

Example:

    Cloud
    ├── Projects
    │   ├── project.json
    │   └── notes.txt
    └── test
        └── example.js

---

# Creating a Cloud Folder

Open:

    Cloud

Click:

    New Folder

Example:

    projects

You can also create nested folders such as:

    projects/test

---

# Creating a Cloud File

Click:

    New File

Example:

    projects/test.js

Enter your content.

Click:

    Save

---

# Editing a Cloud File

Select a file.

Modify its content.

Click:

    Save

---

# Deleting a Cloud File

Select the file.

Click:

    Delete

---

# Cloud Storage Location

Cloud files are stored by the local backend.

The backend uses a directory similar to:

    backend/data/cloud/

This means the current Cloud system is local persistent storage rather than an internet-hosted cloud service.

---

# Settings

RichAF provides interface settings for customization.

Current settings include:

    Auto Refresh
    Saved CSS
    Outline on Load $0
    Backend URL
    Background
    Background Blur
    Background Dim
    Font
    Glass Effects
    Animations

---

# Auto Refresh

Configure:

    Auto-refresh dashboard

For example:

    5

refreshes dashboard information periodically.

Use:

    0

to disable automatic refreshing.

---

# Saved CSS

RichAF can store CSS used by its interface/page tools.

Use:

    Save

after editing your CSS.

---

# Outline on Load $0

When enabled, RichAF can outline the currently selected DevTools element when `$0` is loaded.

---

# Background Customization

RichAF supports custom backgrounds.

You can configure:

    Background Image
    Background Blur
    Background Dim

---

# Background Blur

Increase the blur amount to make the background less visually distracting.

---

# Background Dim

Increase the dim value to darken the background.

This can improve readability when using a bright image.

---

# Interface Font

RichAF's current interface configuration uses a clean system-style font stack.

The default is:

    Arial

---

# Animations

RichAF can enable or disable interface animations.

Use:

    Animations

to control the interface effects.

---

# Backend Settings

RichAF 4.5.6 includes advanced backend settings.

Available configuration includes:

    Host
    Port
    Heartbeat
    CORS Mode
    Maximum JSON Body Size
    WebSocket

---

# Host

Default:

    127.0.0.1

This keeps the server accessible only from the local machine.

---

# Port

Default:

    3210

Therefore the default backend address is:

    http://127.0.0.1:3210

---

# Changing the Port

You can configure another port, for example:

    4000

The backend must then actually listen on that port.

RichAF should also be configured to connect to:

    http://127.0.0.1:4000

Some backend configuration changes require a server restart.

---

# Heartbeat

The heartbeat controls how frequently RichAF checks the backend connection.

This helps detect when the backend goes offline.

---

# CORS

RichAF provides CORS configuration.

Development configurations may allow broader access.

For production deployments, CORS should be restricted to trusted origins.

---

# Maximum JSON Body Size

The backend has a configurable JSON request-body limit.

The current backend parser uses a development-oriented limit around:

    2 MB

The RichAF backend settings allow the configured value to be adjusted within the available range.

Restart the backend when required for parser-level configuration changes.

---

# WebSocket Setting

WebSocket communication can be enabled or disabled.

WebSockets are used for real-time RichAF backend communication.

---

# Backend API

Default API base URL:

    http://127.0.0.1:3210

---

## Health

    GET /api/health

Checks backend health.

---

## Status

    GET /api/status

Returns backend status information.

---

## Setup Status

    GET /api/setup/status

Checks whether backend storage has been initialized.

---

## Initialize

    POST /api/setup

Initializes backend storage.

---

# Configuration API

Get configuration:

    GET /api/config

Update configuration:

    PUT /api/config

---

# Backend Settings API

Get backend settings:

    GET /api/backend/settings

Update backend settings:

    PUT /api/backend/settings

---

# API Connections API

List connections:

    GET /api/connections

Create a connection:

    POST /api/connections

Update a connection:

    PUT /api/connections/:id

Delete a connection:

    DELETE /api/connections/:id

Test a connection:

    POST /api/connections/:id/test

---

# Cloud API

List Cloud items:

    GET /api/cloud/list

Create a folder:

    POST /api/cloud/folder

Read a file:

    GET /api/cloud/file?path=/projects/test.js

Save a file:

    PUT /api/cloud/file

Delete an item:

    DELETE /api/cloud/item?path=/projects/test.js

---

# Background API

Upload a background:

    POST /api/backgrounds/upload

Clear backgrounds:

    DELETE /api/backgrounds

---

# Projects API

List projects:

    GET /api/projects

Create a project:

    POST /api/projects

Delete a project:

    DELETE /api/projects/:id

---

# Events API

Get events:

    GET /api/events

Send an event:

    POST /api/events

Clear events:

    DELETE /api/events

---

# WebSocket API

RichAF connects to:

    ws://127.0.0.1:3210/ws

The backend can send events to connected RichAF clients.

---

# Example WebSocket Message

    {
      "type": "hello",
      "payload": {
        "name": "RichAF Backend",
        "version": "4.5.6"
      },
      "timestamp": 123456789
    }

---

# WebSocket Ping

Client:

    {
      "type": "ping"
    }

Server:

    {
      "type": "pong"
    }

---

# Project Structure

A typical RichAF project looks like:

    RichAF-extension/
    │
    ├── backend/
    │   ├── data/
    │   ├── uploads/
    │   │   └── backgrounds/
    │   ├── package.json
    │   ├── server.js
    │   └── README.md
    │
    ├── icons/
    │   ├── icon16.png
    │   ├── icon48.png
    │   └── icon128.png
    │
    ├── devtools.html
    ├── devtools.js
    ├── manifest.json
    ├── panel.html
    ├── panel.js
    ├── panel.css
    ├── package.json
    ├── start-server.bat
    └── README.md

---

# Development

If you are modifying RichAF itself, the basic development workflow is:

    Edit code
        ↓
    Reload extension
        ↓
    Open DevTools
        ↓
    Open RichAF
        ↓
    Test feature
        ↓
    Check console
        ↓
    Fix issues
        ↓
    Repeat

---

# Reloading the Extension

After changing files such as:

    panel.js
    panel.css
    panel.html
    manifest.json
    devtools.js

open:

    chrome://extensions

Find RichAF.

Click:

    Reload

Then reopen DevTools.

---

# Restarting the Backend

After modifying:

    backend/server.js

restart the backend:

    npm start

---

# Troubleshooting

## RichAF Doesn't Appear

Open:

    chrome://extensions

Check:

    Developer mode = ON
    RichAF = Enabled

Then click:

    Reload

Close and reopen DevTools.

---

# Backend Offline

Make sure Node.js is running.

Run:

    cd backend
    npm install
    npm start

Then check:

    http://127.0.0.1:3210

---

# npm Is Not Recognized

If Windows displays:

    'npm' is not recognized...

Node.js is either not installed or isn't available in PATH.

Install Node.js and reopen your terminal.

---

# Cannot Find server.js

Make sure you are inside the backend directory.

Correct:

    cd RichAF-extension/backend
    npm start

The backend's package.json should reference the backend server correctly.

---

# Port Already in Use

If port 3210 is already occupied, either stop the existing process or choose another port.

Example:

    set RICHAF_PORT=4000

Then:

    npm start

Connect RichAF to:

    http://127.0.0.1:4000

---

# Cloud Doesn't Work

Check:

    Backend is running
    RichAF is connected
    Server URL is correct
    Backend has been initialized

Then try:

    Server → Initialize Server

---

# API Test Fails

Check:

    API Base URL
    Authentication
    Network connection
    Server status

For example:

    https://api.example.com

Make sure the endpoint actually exists and accepts the authentication method you're using.

---

# Sources Doesn't Show a File

The browser can only expose resources that are available through its DevTools/resource APIs.

A server-side file that was never sent to the browser cannot normally appear in Sources.

For example:

    .env
    database.sql
    server.js

may not be available to RichAF when inspecting a normal website.

---

# SCSS Doesn't Appear

If a website compiles:

    styles.scss

into:

    styles.css

the browser may only receive:

    styles.css

RichAF cannot reconstruct source files that were never delivered to the browser.

---

# Cookies Don't Appear

Check:

    You are inspecting the correct website
    The website actually has cookies
    Chrome allows the required extension access
    The current page/domain is correct

---

# Security

RichAF is a development and debugging tool.

Because it interacts with the inspected page and browser APIs, only install RichAF from source you trust.

---

# Backend Security

The default backend is designed for local development.

Default:

    127.0.0.1:3210

Do not casually expose the backend to the public internet.

If you make the backend publicly accessible, you should implement:

    Authentication
    Authorization
    HTTPS
    Rate Limiting
    Request Validation
    Restricted CORS
    Secret Protection
    Access Control

The local RichAF backend should not be considered a production-grade public server by default.

---

# API Secret Security

Do not use RichAF's API Connections storage as a production secrets manager.

Avoid storing highly sensitive credentials such as:

    Production passwords
    Private signing keys
    Database credentials
    Master API keys

in an unsecured development environment.

---

# Recommended Workflow

For general website debugging:

    Dashboard
        ↓
    Sources
        ↓
    Live Edit
        ↓
    Network
        ↓
    Storage
        ↓
    Console
        ↓
    CSS / JSON

---

# Recommended API Workflow

For debugging an existing API request:

    Network
        ↓
    Find request
        ↓
    Inspect request
        ↓
    Save XHR
        ↓
    Replay
        ↓
    Copy Fetch / cURL
        ↓
    Create API Connection

---

# Recommended Backend Workflow

    Server
        ↓
    Connect
        ↓
    Ping
        ↓
    Initialize
        ↓
    API Connections
        ↓
    Cloud
        ↓
    Backend Settings

---

# Example: Debugging an API Request

Suppose a website makes:

    POST /api/login

Open:

    RichAF
        → Network
        → XHR

Find:

    POST /api/login

Open the request.

Inspect:

    Headers
    Payload
    Response

Then click:

    Save XHR

The request is now available in your Saved XHR collection.

You can later:

    Load
    Edit
    Replay
    Update Saved
    Delete
    Copy Fetch
    Copy cURL

---

# Example: Testing a Mock Response

Suppose the real API returns:

    {
      "premium": false
    }

You want to test your frontend with:

    {
      "premium": true
    }

Go to:

    Network
        → Override

Set the URL match to the API endpoint.

Select:

    Mock Response

Set the response body:

    {
      "premium": true
    }

Click:

    Install Fetch Override

The matching request can now be tested against the mocked response.

---

# Example: Simulating a Slow API

Set:

    Delay:
    2000

Then install the override.

Your frontend can now be tested against an artificially delayed request.

This is useful for checking:

    Loading screens
    Spinners
    Skeleton UI
    Timeout handling
    Error handling

---

# Example: Editing a Website Element

Select an element in Chrome DevTools.

Open:

    RichAF → Live Edit

Click:

    Load $0

Change:

    Text Content

Click:

    Apply Text

The change will appear immediately on the live page.

You can also modify:

    Attributes
    Inline CSS
    Visibility

---

# Example: Creating a Cloud Workspace

Start the backend.

Open:

    Cloud

Create:

    New Folder

Name it:

    MyProject

Then create:

    MyProject/notes.txt

Enter:

    API debugging notes

Click:

    Save

The file will be stored in the backend's Cloud directory.

---

# Architecture

RichAF consists of two major components:

    RichAF Extension
            |
            |
            +--------------------+
            |                    |
            v                    v
       Browser Side          Backend
            |                    |
            |                    +── Cloud
            |                    +── API Connections
            |                    +── Events
            |                    +── Projects
            |                    +── Settings
            |                    +── Backgrounds
            |
            +── Sources
            +── DOM
            +── Network
            +── Console
            +── Cookies
            +── Storage
            +── Page JavaScript

Browser-side functionality works directly with the inspected webpage and Chrome DevTools APIs.

Backend functionality provides persistence and server-side features.

---

# What RichAF Does Not Do

RichAF does not automatically:

- Access arbitrary server-side source code.
- Reveal files that were never sent to the browser.
- Bypass website authentication.
- Turn the local backend into a secure production server.
- Make API secrets automatically secure.
- Permanently modify a website's source code simply by editing its live DOM.
- Upload browser cookies to the RichAF backend automatically.

RichAF is primarily a development, debugging, testing, and experimentation environment.

---

# Tech Stack

## Chrome Extension

    Manifest V3
    JavaScript
    HTML
    CSS
    Chrome DevTools APIs
    Chrome Storage APIs
    Chrome Cookies APIs

## Backend

    Node.js
    Express
    WebSocket
    Multer
    CORS
    Local JSON storage

---

# Contributing

To contribute to RichAF:

1. Fork the repository.
2. Clone the repository.
3. Install the backend dependencies.
4. Load the extension into Chrome.
5. Start the backend if needed.
6. Make your changes.
7. Test the extension.
8. Test the backend.
9. Commit your changes.
10. Open a pull request.

---

# Development Requirements

Recommended:

    Google Chrome
    Node.js 18+
    npm
    Git

---

# Quick Start

Install the extension:

    chrome://extensions
        ↓
    Developer Mode
        ↓
    Load Unpacked
        ↓
    Select RichAF-extension

Start the backend:

    cd backend
    npm install
    npm start

Connect RichAF:

    DevTools
        ↓
    RichAF
        ↓
    Server
        ↓
    Connect

Then explore:

    Dashboard
    Sources
    Live Edit
    Network
    Storage
    Console
    CSS
    JSON
    Tools
    Server
    Cloud
    Settings

---
**RichAF 4.5.6**

