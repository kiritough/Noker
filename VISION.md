# Noker Vision

Your files are already there. Noker just makes them make sense.

---

## The Problem

Every tool that tries to help you organize information eventually does the same thing: it takes your files and makes them its files.

You get structure, but lose ownership. You get features, but lose portability. You get an app, and when the app is gone — so is the context around your work.

This trade-off is so common that most people don't question it anymore.

Noker does.

---

## What Noker Is

Noker is a local-first workspace that sits on top of your existing files — without touching them, moving them, or locking them inside a proprietary format.

Your files stay files. Your folders stay folders. Your data stays yours.

Noker adds a layer of structure, meaning, and relationships on top of what's already there. That layer is separate from your content, transparent in how it works, and completely removable.

Delete Noker tomorrow. Your files are still there — unchanged, readable, free.

---

## Core Principles

**Local First.** Noker runs entirely on your machine. No cloud account, no remote server, no internet connection required, no subscription, no lock-in. Your device is the environment. Your storage is the source of truth.

**Files belong to you — not to the app.** Noker may store additional workspace data, but it does so in a separate layer, without ever modifying your original files. If Noker disappears, your files remain exactly as you left them. This is not a feature. This is a guarantee.

**You decide how to work.** Noker doesn't impose a workflow. Use Explorer and open files one by one. Build a Workspace with a full project canvas. Combine multiple files into a single working environment — or don't. Every approach is valid. The system adapts to you, not the other way around.

**Simple entry, real depth.** The first thing you see in Noker should make sense immediately. Complexity doesn't greet you at the door — but the depth is there when you need it.

**Open by design.** Noker is open-source under the MIT license. The code is readable, the format is inspectable, and every architectural decision is visible. Nothing is hidden behind abstraction.

---

## How You Enter Noker

Noker doesn't force a single way to start.

When you open the app, you choose how to begin: pick a folder and browse it in Explorer, open an existing Workspace, create a new one, or start from a blank canvas. The entry point adapts to how you work — not the other way around.

---

## Two Environments, One Workspace

### Explorer

Explorer is a direct window into your real file system — not a reimagined abstraction of it.

You see the actual files and folders on your device. You browse directories, open and edit files, move things around, search content. What you do in Explorer reflects immediately on disk, because Explorer *is* the disk.

It works with reality as it is.

### Workspace

Workspace is not a note-taking environment.

It's an environment for thinking, organizing, and connecting information — built on top of files that already exist on your device, without moving or copying any of them.

You pull files from different locations across your device and arrange them into a single project canvas. What you see in Workspace looks like one unified environment — an introduction from one file, a main body from another, a conclusion from a third. But underneath, these are separate files sitting exactly where they always were on your disk. No copies. No merging. No touching the originals.

You work inside one canvas without switching between files. The files remain files — Workspace just presents them as a unified whole.

This is not the only way to use Workspace. If you prefer to work with files individually, switching between them as needed — that works too. Noker doesn't require you to build a multi-file canvas. It's a capability, not a rule. Use it when it makes sense for your work.

A file can exist in multiple Workspaces at the same time. The file stays where it is; Workspace just knows about it and builds context around it.

The purpose of Workspace is not storage. The purpose of Workspace is thinking.

### Workspace and Projects

A Workspace is the environment where you work. A project is the unit of work inside it.

They are the same concept — a project canvas — viewed at different scales. One Workspace can contain a single focused project, or it can hold several. A project is not a folder. It's a structured environment that can pull together files from different directories, notes, OPV relationships, and any other Noker object — all without those files ever leaving their original locations on disk.

---

## Navigation and Relationships

One of the core architectural decisions in Noker is keeping navigation and relationships as separate concepts.

Most tools collapse them into a single linking system. The result is that links end up meaning too many things at once — and eventually nothing in particular.

### `[[ ]]` — Navigation

Double brackets handle document structure and movement.

```
[[Introduction]]
[[Planning]]
[[Architecture]]
[[Conclusion]]
```

They generate a table of contents. They create jump points inside a document. That's their job, and it's the only job they do.

Double brackets don't express semantic relationships between objects. They answer one question: *where am I inside this document?*

### OPV — Object Path View

OPV is the relationship layer at the core of Noker.

```
>Object or note<
```

An OPV is not a link. It's not a tag. It's not a mention.

An OPV is a directed reference — one object pointing to another and saying: *to fully understand me, you also need this.*

What makes OPV powerful is its universality. An OPV can point to anything:

- A note or a piece of text
- A file or a folder
- A project
- A URL or an external resource
- A reminder or a comment
- Any object inside Noker

The meaning of an OPV connection depends entirely on how the user chooses to use it. Noker doesn't impose a category. The user defines the intent.

**Example:**

```
How to cook mashed potatoes
>Buy ingredients<
>Choose the right potatoes<
>Cooking course reference<
```

Each `>connection<` is a stored, traversable reference. Not a decoration — a real relationship between two objects.

When connections multiply, Noker collapses them into a compact form:

```
How to cook mashed potatoes >OPV<
```

Expand it, and the full reference map appears. The document stays readable; the structure stays intact.

OPV connections are also recursive. Each connected object can have its own OPV references, which in turn have their own. The structure grows as deep as the work requires — automatically, without any manual graph building.

```
How to cook mashed potatoes
  >Choose the right potatoes<
      >Potato varieties<
      >Fresh vs stored potatoes<
  >Buy ingredients<
```

The deeper you go, the richer the knowledge structure becomes. And none of it was drawn manually.

OPV is also designed to be fast. You don't select text and click a button. You type `>note<` inline, and Noker saves the reference automatically. The connection exists the moment you write it.

---

## Two Modes

Noker separates the act of writing from the act of reading.

In **edit mode**, you see everything — text, OPV connections, navigation markers, the full structure of your document. This is where you build.

In **view mode**, the document becomes clean. OPV markers are hidden. Navigation is quiet. What remains is the content itself — readable, focused, distraction-free.

The structure doesn't disappear in view mode. It's still there, stored in the `.noker` layer, ready the moment you switch back to editing.

---

## Graphs

Noker has a graph view — but you never build it manually.

When you write and create OPV connections, Noker stores every relationship automatically. The graph is a consequence of that work, not a separate maintenance task. Open it at any point, and it reflects the actual structure of your projects — built from real work, not from sessions spent drawing diagrams.

This is the difference between a graph that shows you what you know and a graph that shows you what you were supposed to organize.

---

## The `.noker` Layer

All workspace data — structure, relationships, project organization, navigation, metadata — is stored in a separate `.noker` layer alongside your files.

Your original files are never modified. The `.noker` layer holds the context; your files hold the content. They are independent of each other, and that independence is intentional.

---

## Privacy and Security

Noker doesn't send anything anywhere.

Your data never leaves your device. The `.noker` layer stores only structure, relationships, and metadata — never the content of your files. Your files are read locally, edited locally, and saved locally.

There are no telemetry calls, no usage tracking, no background connections. What's on your machine stays on your machine.

---

## Sharing and Export

When you're ready to share or export your work, Noker gives you the choice — not the format.

**Export as a single file.** Combine the entire Workspace into one merged document. Everything in one place, ready to send or publish.

**Export as a ZIP.** Get your original files as they are — clean, unmodified, no Noker-specific format. Just your files in a folder.

**Share as `.nkr`.** The full Workspace package: all files, all OPV relationships, complete structure and context. The recipient opens it in Noker and sees the project exactly as you left it. Sharing transfers knowledge, not just files.

You decide what to share and how. Noker doesn't lock you into one format.

---

## What Noker Is Not

Noker is not a cloud platform, a note-taking service, a social tool, or a proprietary ecosystem. It doesn't try to replace your file system or your operating system. It's not a clone of Obsidian, and it's not a clone of VS Code.

It learns from existing tools where useful. But its goal is different from all of them.

---

## The Vision

Most tools are built on the assumption that your files need to be rescued — moved into a special place, reformatted, managed by the application.

Noker starts from the opposite assumption: your files are fine where they are. What's missing is a layer that understands them — one that adds structure without creating dependency, and builds meaning without building walls.

That's what Noker is building.

A workspace where knowledge stays portable. Projects stay understandable. Data stays local. And you stay in control.

---

*github.com/kiritough/Noker*
