# FormCMS: The AI-Powered App Platform

[![NuGet](https://img.shields.io/nuget/v/FormCMS)](https://www.nuget.org/packages/FormCMS)
[![.NET 10](https://img.shields.io/badge/.NET-10-512BD4)](https://dotnet.microsoft.com/download)
[![Docker Pulls](https://img.shields.io/docker/pulls/jaike/formcms-mono)](https://hub.docker.com/repository/docker/jaike/formcms-mono)
[![License: MIT](https://img.shields.io/github/license/formosora/formcms)](LICENSE)

FormCMS is an open-source platform that turns natural language into full-stack apps — schemas, APIs, UI, and deployment — in minutes. Ship with Docker, build with AI agents, scale to millions of records.

---

## ✨ Why FormCMS?

<table>
<tr>
<td align="center" width="33%">
<h3>🤖 AI-Powered</h3>
<p>Generate schemas, data, GraphQL queries, and full UI pages from natural language — in the browser or through AI agents.</p>
</td>
<td align="center" width="33%">
<h3>🔌 MCP Server Built-In</h3>
<p>AI agents (Antigravity, Cursor, Codex) connect directly via MCP to design schemas, seed data, and deploy apps — all from the chat window.</p>
</td>
<td align="center" width="33%">
<h3>🚀 Scalable & Performant</h3>
<p>P95 latency under 200ms, 2,400+ QPS throughput. SQLite, PostgreSQL, SQL Server, and MySQL supported.</p>
</td>
</tr>
</table>

---

## 🎥 In Action

Watch FormCMS build a complete Library system (Entities, Data, Queries, and UI) from scratch in under 60 seconds (sped up 10x).

[![FormCMS Demo](https://img.youtube.com/vi/lqjuDNLLaBY/maxresdefault.jpg)](https://www.youtube.com/watch?v=lqjuDNLLaBY)

*Click the image above to watch the full demo on YouTube.*

### 🛠️ Build Full-Stack React Apps using AI Agents (MCP)

Learn how to connect different AI editors to the FormCMS MCP server to scaffold, build, and deploy apps without writing any backend code:

<table width="100%">
<tr>
<td align="center" width="33%">
<strong>Antigravity IDE</strong>
<a href="https://www.youtube.com/watch?v=D0YpabyIIVQ">
<img src="https://img.youtube.com/vi/D0YpabyIIVQ/maxresdefault.jpg" width="100%" alt="Antigravity IDE Tutorial" />
</a>
<br/>
<sub><a href="https://www.youtube.com/watch?v=D0YpabyIIVQ">Watch Tutorial →</a></sub>
</td>
<td align="center" width="33%">
<strong>VS Code + Codex</strong>
<a href="https://www.youtube.com/watch?v=ScFz08tMOnA">
<img src="https://img.youtube.com/vi/ScFz08tMOnA/maxresdefault.jpg" width="100%" alt="VS Code + Codex Tutorial" />
</a>
<br/>
<sub><a href="https://www.youtube.com/watch?v=ScFz08tMOnA">Watch Tutorial →</a></sub>
</td>
<td align="center" width="33%">
<strong>Cursor AI</strong>
<a href="https://www.youtube.com/watch?v=Vr7xcrD5Jd8">
<img src="https://img.youtube.com/vi/Vr7xcrD5Jd8/maxresdefault.jpg" width="100%" alt="Cursor AI Tutorial" />
</a>
<br/>
<sub><a href="https://www.youtube.com/watch?v=Vr7xcrD5Jd8">Watch Tutorial →</a></sub>
</td>
</tr>
</table>

---

## 🛠️ Three Ways to Build

<table>
<tr>
<td align="center" width="33%">
<h3>🌐 Beginners</h3>
<p><strong>No IDE needed.</strong> Open FormMate in your browser, describe what you want in plain English — AI generates your schemas, sample data, queries, and pages.</p>
<p><a href="https://demo.formcms.com/mate">Try the live demo →</a></p>
</td>
<td align="center" width="33%">
<h3>🎨 Frontend Developers</h3>
<p><strong>Build with AI agents.</strong> Connect Antigravity, Cursor, or Codex to the built-in MCP server — the agent designs your schema, writes your React app, and deploys it.</p>
<p><a href="https://github.com/formcms/formcms/wiki/Build-a-Full%E2%80%90Stack-React-App-with-FormCMS-and-AI-Agents-(Antigravity,-Cursor,-Codex)">AI agent setup guide →</a></p>
</td>
<td align="center" width="33%">
<h3>⚙️ Full-Stack Developers</h3>
<p><strong>Extend the platform.</strong> FormMate is Node.js (Fastify), FormCMS is .NET — fork the repo, add custom endpoints, write plugins, or integrate external services.</p>
<p><a href="https://github.com/formcms/formcms/wiki/Setup.md">Dev setup guide →</a></p>
</td>
</tr>
</table>

### 🏗️ Built with FormCMS

| App | Description |
|-----|-------------|
| **[Zen Health Tracker](https://zen.formcms.com/)** | A full health tracking app built in hours using FormCMS + AI agent — zero manual coding. |
| **[Stash PWA](https://demo.formcms.com/stash/)** | A PWA companion app — bookmark, listen (TTS), and cache FormCMS content offline. |

---

## 🚀 Quick Start

> **🟢 Don't want to install?** Try the [live demo](https://demo.formcms.com/mate) instantly — login: `sadmin@cms.com` / `Admin1!`

Pull and run from [Docker Hub](https://hub.docker.com/repository/docker/jaike/formcms-mono):

```bash
docker run -d \
  --name formcms \
  -p 5000:5000 \
  -v formcms_data:/data \
  -e DATABASE_PROVIDER=0 \
  -e "CONNECTION_STRING=Data Source=/data/cms.db" \
  -e FORMCMS_DATA_PATH=/data \
  jaike/formcms-mono:latest
```

| Service | URL |
|---------|-----|
| Admin portal (FormMate) | `http://localhost:5000/mate` |
| REST API | `http://localhost:5000/api/` |
| **MCP server (SSE)** | **`http://localhost:5000/mcp/sse`** |

> **📌 Try these prompts in FormMate:** *"Design entities for a library system"* · *"Add sample data for books"* · *"Create a query to display all books"*
>
> **🤖 Using an AI agent?** Point it at `http://localhost:5000/mcp/sse` to start building via MCP tools.

For production deployment with PostgreSQL, see the [Docker Hub page](https://hub.docker.com/repository/docker/jaike/formcms-mono). Want to contribute or run from source? See the [Development Setup Guide →](https://github.com/formcms/formcms/wiki/Setup.md)

---

## 🔨 Build from Source

**Prerequisite:** [.NET 10 SDK](https://dotnet.microsoft.com/download)

```bash
git clone https://github.com/formosora/formcms.git
cd formcms

dotnet build formcms.sln

# All-in-one host: REST API + GraphQL + MCP server
dotnet run --project server/FormCMS.MonoApp
# → http://localhost:5000  (API: /api · MCP: /mcp/sse)

# Test suite
dotnet test server/FormCms.Course.Tests
```

Notes:

- The browser admin portal (**FormMate**) is a separate Node.js/React app. In development, MonoApp reverse-proxies `/mate` to the FormMate dev server on `127.0.0.1:3001`; the Docker image above bundles everything prebuilt, so use it for the full out-of-box UI experience.
- The Course demo and the per-database examples are orchestrated with **.NET Aspire** (Docker Desktop required), e.g. `dotnet run --project server/FormCMS.Course.AppHost`.

---

## 🧰 Tech Stack

| Layer | Technology |
|-------|------------|
| Backend | .NET 10 / ASP.NET Core (C# 14) |
| Data access | EF Core 10 · SqlKata · FluentMigrator |
| Databases | SQLite · PostgreSQL · SQL Server · MySQL · MongoDB |
| APIs | REST · GraphQL (GraphQL.NET + GraphiQL) · MCP over SSE |
| Caching & messaging | HybridCache · Redis (RedLock) · Kafka · NATS |
| Admin UI | FormMate portal (Node.js/Fastify + React), served prebuilt from the mono image |
| Orchestration & ops | Docker · Kubernetes manifests (`etc/k8s_deploy`) · .NET Aspire · MkDocs |

---

## 📁 Repository Structure

```
├── server/
│   ├── FormCMS/                          # Core engine — published as the `FormCMS` NuGet package
│   ├── FormCMS.MonoApp/                  # All-in-one host (API + MCP + assets) — base of the Docker image
│   ├── FormCMS.Course/                   # Full-featured course/demo application
│   ├── FormCMS.Course.AppHost/           # .NET Aspire orchestration host
│   ├── FormCMS.Course.ServiceDefaults/   # Aspire shared service defaults
│   └── FormCms.Course.Tests/             # Automated test suite
├── examples/                             # Per-database starters: SqliteDemo · PostgresDemo · SqlServerDemo · MysqlDemo
├── YoutubeDownloader/                    # Example plugin (YoutubeExplode-based asset downloader)
├── etc/                                  # Ops extras: k8s_deploy, performance_tests, pg-replica, schema-ui, sqlserver-fts
├── doc/                                  # Documentation sources: readme-parts, mkdoc (MkDocs), wiki assets, diagrams
└── formcms.sln                           # Visual Studio solution (14 projects)
```

---

## 📚 Learn More

📖 [Documentation Wiki](https://github.com/formcms/formcms/wiki) · [Architecture](https://github.com/formcms/formcms/wiki/Architecture.md) · [Performance & Scalability](https://github.com/formcms/formcms/wiki/Performance-Scalability.md) · [Setup Guide](https://github.com/formcms/formcms/wiki/Setup.md)

In this repo: [System design notes](doc/wiki/system-design-formCMS.md) · [Query performance](doc/wiki/query-performance.md)

---

## 🗺️ Roadmap

FormCMS is actively evolving toward a vision of **AI-native app development**:

| Phase | Focus | Key Features |
|-------|-------|-------------|
| **Enhanced AI** | Smarter generation | Natural language → schema, AI-suggested relationships, auto-generated CRUD & queries |
| **Visual Builder** | No-code editing | Drag-and-drop page builder, visual schema editor, real-time preview, theme templates |
| **Marketplace** | Community ecosystem | Pre-built app templates, community components, one-click install |

> **The Vision:** Describe your app in plain English → AI generates the entire backend → deploy with one click.

---

## 🤝 Contributing

Issues and pull requests are welcome. For larger changes, open an issue first to discuss the direction. To get your environment running, see [Build from Source](#-build-from-source) above and the upstream [Development Setup Guide](https://github.com/formcms/formcms/wiki/Setup.md).

## 📄 License

[MIT](LICENSE) © FormCMS.

> This repository mirrors the open-source [FormCMS](https://github.com/FormCMS/formcms) project. The live demo, documentation wiki, Docker images, and YouTube tutorials linked above are hosted by the upstream project.
