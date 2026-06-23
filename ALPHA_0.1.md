# Noker — Alpha 0.1

The first release of Noker. Not a prototype, not a demo — a working product with a real philosophy inside.

Noker is built around a simple idea: files should not feel complicated. They should be easy to read, easy to connect, easy to organize, and easy to keep forever.

Built with Kotlin Multiplatform. Runs on macOS, Windows, and Android.

---

## Local-First

Noker runs entirely on your device.

No cloud. No server. No account. No subscription. Your files never leave your machine — not when saving, not when creating connections, not when organizing projects.

Your device is the workspace. Your storage is the source of truth. Everything else is optional.

---

## Explorer

A direct window into your real file system.

When you launch Noker, you choose a working folder. The folder tree appears on the left, its contents on the right. Everything you see in Explorer is the actual files on your disk — no abstractions, no repackaging.

**Supported formats:**

Text and documents — `.txt`, `.md`, `.log`, `.csv`, `.json`, `.xml`, `.yaml` — open, edit, and save.

Code — `.kt`, `.java`, `.py`, `.js`, `.html`, `.css`, `.cpp`, `.c`, `.cs`, `.go`, `.rs`, `.swift`, `.sh`, `.bat` — open and edit as plain text.

Any other format — open directly in an external application from inside Noker.

**What works:**

- Browse folders and files
- Create, rename, and delete files and folders
- Right-click context menu — open, edit, rename, delete, properties
- Save with Ctrl+S
- Automatic backup on every save — the previous version is copied to `nokerbecap` with a timestamp; the original is never lost
- Open any file in an external application
- Basic command line: `help`, `ls`, `cd`, `mkdir`, `rm`
- On macOS and Windows — access to the native system terminal under the hood

---

## Workspace

Workspace is not a folder and not a storage system. It's a layer built on top of your existing files — an environment for thinking and organizing information.

You create a Workspace and pull files into it from anywhere on your device. The files stay where they are — Workspace just knows about them and builds context around them.

Multiple files from different directories can appear in Workspace as a single project canvas — an introduction from one file, a main body from another, a conclusion from a third. You work inside one environment without switching between files. Underneath, these are separate files sitting exactly where they always were. No copies. No merging. Originals untouched.

This is not the only way to work. If you prefer to open files one by one and switch between them — that works too. Noker doesn't impose a workflow. Use the canvas when it makes sense, work with files directly when it doesn't.

A file can exist in multiple Workspaces at the same time without copying. Remove a file from a Workspace — the original stays on disk, untouched.

---

## Editor

The Noker editor works with text and code. No clutter — just what you need to get work done.

**Markdown formatting:**

- Headings H1, H2, H3
- Bold and italic
- Bulleted and numbered lists
- Horizontal separator

**Two modes:**

In edit mode, you see everything — text, OPV connections, navigation markers, the full document structure. This is where you build.

In view mode, the document becomes clean. Markdown is rendered. OPV markers are hidden. What remains is the content itself — readable and focused.

**Search inside a file** — Ctrl+F. Fast search within the open document.

---

## OPV — Object Path View

The relationship layer at the core of Noker.

```
>Object or note<
```

An OPV is not a link and not a tag. It's a directed reference — one object pointing to another and saying: *to fully understand me, you also need this.*

An OPV does not define what a relationship means. It only declares that a relationship exists. The meaning belongs to the user.

An OPV can point to anything: a note, a piece of text, a file, a folder, a project, a URL, any object inside Noker.

**Example:**

```
Project plan
>roadmap.md<
>Design mockup<
>Repository link<
```

Each `>connection<` is a real, stored reference between two objects. Not a decoration.

When connections multiply, Noker collapses them into a compact form:

```
Project plan >OPV<
```

Expand it, and the full reference map appears. The document stays readable; the structure stays intact.

Creating OPV connections is fast — no need to select text or open a menu. Type `>note<` inline, and Noker saves the connection automatically. The relationship exists the moment you write it.

---

## `[[ ]]` — Navigation

Double brackets create document structure and fast jump points.

```
[[Introduction]]
[[Architecture]]
[[Conclusion]]
```

Noker builds a table of contents from these. This is a navigation tool — it does not create relationships between objects. It only helps you move through a document.

---

## Graph Foundation

In Alpha 0.1, the graph is not visualized. But the foundation is already running.

Every time you create an OPV connection, Noker stores that relationship in the `.noker` layer. Connections accumulate automatically as you work. By the time graph visualization arrives, the knowledge structure will already be built from real work — not drawn by hand.

---

## Search

Search in Noker works within your Workspace — not across the entire file system, only across what you've added to your working context.

Search covers:

- File and folder names
- Content of text files
- OPV connections

Results are fast — file name and the matching text excerpt.

---

## The `.noker` Layer

Everything Noker creates — Workspace structure, OPV connections, navigation, metadata — is stored in a separate `.noker` layer alongside your files.

Original files are never modified. The `.noker` layer holds the context; your files hold the content. They are fully independent of each other.

Delete Noker — your files remain exactly as you left them.

---

## Export and Sharing

When you're ready to share or export your work, Noker gives you the choice — not the format.

**Single file.** The entire Workspace is merged into one document. Everything in one place, ready to send or publish.

**ZIP archive.** Your original files as they are — clean, no Noker-specific format. Just your files in a folder.

**`.nkr` package.** Noker Package — the full Workspace bundle: all files plus the `.noker` layer with all connections and structure. The recipient opens it in Noker and sees the project exactly as you left it. What's transferred is not a set of files — it's a working environment.

You decide what to share and how. Noker doesn't lock you into a format.

---

## Platforms

Noker is built with Kotlin Multiplatform — one codebase for all platforms.

- **macOS** — full version with terminal
- **Windows** — full version with terminal
- **Android** — graphical interface, terminal not available

---

*github.com/kiritough/Noker*
