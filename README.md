<p align="center">
    <a href="https://flet.dev/">
        <img style="background: #fff; padding: 30px; border-radius: 5px; width: 400px;" src="https://github.com/flet-dev/flet/raw/main/media/logo/flet-logo.svg" alt="flet logo">
    </a>
</p>

<h3 align="center">The fastest way to build Flutter apps in Python</h3>

<p align="center">Flet enables developers to easily build realtime web, mobile and desktop apps in Python. No frontend experience required</p>

### ⚡From idea to app in minutes

An internal tool or a dashboard for your team, weekend project, data entry form, kiosk app, or high-fidelity prototype - Flet is an ideal framework to quickly hack great-looking interactive apps to serve a group of users.

### 📐 Simple architecture

No more complex architecture with JavaScript frontend, REST API backend, database, cache, etc. With Flet you just write a monolith stateful app in Python only and get multi-user, real-time Single-Page Application (SPA).

### 🔋Batteries included

To start developing with Flet, you just need your favorite IDE or text editor. No SDKs, no thousands of dependencies, no complex tooling - Flet has a built-in web server with assets hosting and desktop clients.

### <img src="https://github.com/flet-dev/flet/raw/main/media/flutter/icon_flutter.svg" height="20px" /> Powered by Flutter

Flet UI is built with [Flutter](https://flutter.dev/), so your app looks professional and could be delivered to any platform. Flet simplifies the Flutter model by combining smaller "widgets" to ready-to-use "controls" with an imperative programming model.

### 🌐 Speaks your language

Flet is language-agnostic, so anyone on your team could develop Flet apps in their favorite language. [Python](https://flet.dev/docs/guides/python/getting-started) is already supported, Go, C# and others are [coming next](https://flet.dev/roadmap).

### 📱 Deliver to any device

Deploy Flet app as a web app and view it in a browser. Package it as a standalone desktop app for Windows, macOS, and Linux. Install it on mobile as [PWA](https://web.dev/what-are-pwas/) or view via Flet app for iOS and Android.

## Running locally for development

- Install dependencies `pip install -r requirements.txt`

- Start the flet development server `flet main.py`

This will open a new window and any changes made to main.py will be automatically reflected


## What makes this work on Railway?

- **Custom build plan:** [nixpacks.toml](https://github.com/brody192/reflex-template/blob/main/nixpacks.toml)

    - Sets the environment variable `GIN_MODE` to `release` for production purposes
    - Installs two needed system libraries `libgtk-3-0` and `libgstreamer1.0-0`

- Have Flet listen on `$PORT`

    - Setting `port` to `int(os.getenv("PORT", 8502))` in the `ft.app` constructor, This allows Railway to properly route traffic to and from the Flet app