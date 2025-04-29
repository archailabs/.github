# ChainGraph v2

![ChainGraph logo](../images/dark_bg.png#gh-dark-mode-only)
![ChainGraph logo](../images/light_bg.png#gh-light-mode-only)

[![License](https://img.shields.io/badge/license-BSL-blue.svg)](LICENSE.txt)

ChainGraph is a source-available, flow-based programming framework that empowers developers to visually design, execute, and manage complex computational graphs. Whether you're building custom AI agents, data processing pipelines, or collaborative automation systems, ChainGraph's modular architecture, strong type-safety guarantees, and real-time features help you build robust workflows efficiently.

> **Disclaimer:** This version is intended for demonstration and experimentation purposes only. The API and internal architecture are still evolving, and breaking changes may occur as new features are added and improvements are made.

## Table of Contents

- [Key Features](#key-features)
- [Architecture & Technologies](#architecture--technologies)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Running in Development Mode](#running-in-development-mode)
- [PostgreSQL Database Storage](#postgresql-database-storage)
- [Building for Production](#building-for-production)
- [Docker & Docker-compose](#docker--docker-compose)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [Development Tools](#development-tools)
- [Current Limitations & Work-In-Progress](#current-limitations--work-in-progress)
- [Release Process](#release-process)
- [Developer Documentation](#developer-documentation)
- [License](#license)

## Key Features

- **Type-Safe Port System:**
  Supports a rich set of port types including primitives (string, number, boolean) and complex types (arrays, objects, streams, enums). Each port is defined with its own configuration and runtime validation (via Zod and SuperJSON) and employs both lazy instantiation and caching for optimal memory usage.

- **Modular and Extensible Nodes:**
  Create custom nodes using decorators and metadata. Nodes feature multiple input and output ports and integrate seamlessly into the flow builder, enabling rapid development of complex workflows.

- **Visual Flow Editor:**
  Build flows graphically with a React- and XYFlow-based frontend. Enjoy features like drag-and-drop layout, zoom and pan, resizing, contextual menus, and live previews.

- **Robust Execution Engine & Debugging Tools:**
  A backend execution engine supports concurrent execution of flows with real-time event subscriptions, plus debugging features such as breakpoints, step-over, and detailed event logging for effective troubleshooting.

- **Real-Time Synchronization & Optimistic Updates:**
  Integrated with tRPC and Effector for end-to-end type safety, the system provides real-time updates (via WebSockets) and supports optimistic UI updates—ensuring an interactive and responsive user experience.

- **Docker and Cloud Compatibility:**
  Easily build, deploy, and scale both the backend and frontend using Docker and docker-compose. Containerized deployment simplifies the setup process and enhances portability.

## Architecture & Technologies

ChainGraph is built with modern web technologies, aiming at a robust and type-safe development experience:

- **TypeScript:**
  Uses advanced TypeScript features (generics, decorators, conditional types) for compile-time safety and robustness.

- **Effector:**
  A reactive state management library that powers both frontend and backend state handling and simplifies the implementation of optimistic updates and subscriptions.

- **tRPC:**
  Facilitates end-to-end type-safe API communication between the frontend and backend, minimizing runtime errors and ensuring consistency in data handling.

- **Zod & SuperJSON:**
  Zod is used for runtime schema validation, while SuperJSON manages complex data serialization, ensuring that data remains consistent across the client and server boundaries.

- **XYFlow:**
  A visual flow library used on the frontend to render and manage the drag-and-drop canvas, enabling users to compose workflows visually.

- **WebSockets:**
  Real-time subscriptions using WebSocket (via tRPC's adapter) keep the client in constant sync with backend state and execution events.

## License

ChainGraph is licensed under a [Business Source License 1.1 (BUSL-1.1)](LICENSE.txt).

Since version 1.0 refer to a table below showing a conversion dates for each version:

| ChainGraph Version | License | Converts to Apache 2.0 |
| ------------------ | ------- | ---------------------- |
