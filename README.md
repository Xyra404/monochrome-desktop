# Monochrome Desktop

A lightweight Tauri desktop app built with vanilla HTML, CSS, and JavaScript, backed by a Rust runtime.

I am in no way affiliated with Monochrome, nor its developers.

## Overview

This project is a Tauri-powered desktop shell for Monochrome. It includes:

- A native desktop window configured in `src-tauri/tauri.conf.json`
- A simple local UI in `src/index.html`, `src/styles.css`, and `src/main.js`
- A Rust backend in `src-tauri/src/lib.rs` exposing a Tauri command (`greet`)
- Packaging metadata and icons for desktop distribution

> In production, the app window is configured to open `https://monochrome.tf/`, while the local frontend files provide a development starter experience.

## Features

- Native Tauri window with desktop integration
- Vanilla JS frontend without a framework
- Rust backend with Tauri command support
- Example greeting command bridging the frontend and Rust

## Project Layout

- `package.json` — frontend package metadata and development script
- `src/` — frontend assets and app entrypoints
- `src-tauri/` — Tauri configuration and Rust source code
- `src-tauri/tauri.conf.json` — app settings, window settings, and bundle configuration

## Prerequisites

- Node.js (recommended latest LTS)
- Rust toolchain

## Getting Started

```bash
npm install
npm run tauri dev
```

This launches the app in development mode and loads the local frontend.

## Build

To build a production desktop bundle:

```bash
npm run tauri build
```

## Extending the App

- Update `src/index.html` and `src/styles.css` for UI changes
- Add frontend logic in `src/main.js`
- Register new Rust commands in `src-tauri/src/lib.rs`
- Configure app behavior and windows in `src-tauri/tauri.conf.json`

## Recommended IDE Setup

- VS Code
- `rust-analyzer`
- Tauri extension for VS Code
- Optional: [Prettier](https://prettier.io) for formatting frontend files
