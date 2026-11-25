# OAI Toolkit

**Download, preserve, organize, and explore your ChatGPT conversations.**

OAI Toolkit brings together three independent tools developed by **Corrosion Labs**. They form a practical workflow for keeping local copies of ChatGPT content, converting those copies into readable documents, and exploring the resulting knowledge in Obsidian.

This repository is a **guide to the toolkit**, not a combined installer or a copy of the three applications. Each tool has its own repository, documentation, and release cycle.

## How the tools work together

```text
ChatGPT account
      |
      v
OAI-Downloader
Download conversations and associated resources to a local backup
      |
      v
OAI-Processor
Process the backup and export organized Markdown documents
      |
      v
Obsidian vault
      |
      v
Concept Indexer
Find concepts, create wikilinks, and build thematic indexes
```

OAI-Processor can also export **HTML** for reading outside Obsidian. Concept Indexer is optional: the exported Obsidian vault can be used without it.

## 1. OAI-Downloader — Preserve

OAI-Downloader connects to ChatGPT, examines projects and conversations, builds a resource inventory, and downloads the data to local storage. It supports selective downloads and records download results to help manage subsequent runs.

- **Repository:** [CorrosionLabs/OAI-Downloader](https://github.com/CorrosionLabs/OAI-Downloader)
- **User manual:** [OAI-Downloader documentation](https://corrosionlabs.github.io/documentation/OAI-downloader/)

## 2. OAI-Processor — Organize and export

OAI-Processor reads the local backup created by OAI-Downloader. It analyzes and processes projects, conversations, and associated resources, then exports the results as Markdown documents for an **Obsidian vault** or as **HTML**.

Processing and exporting are separate steps, so processed information can be exported again using different options without repeating the entire processing stage when the source data has not changed.

For large Obsidian imports, an optional assisted export copies projects sequentially and waits for Obsidian's indexing activity between projects. This mode requires the **Local REST API** community plugin in Obsidian.

- **Repository:** [CorrosionLabs/OAI-Processor](https://github.com/CorrosionLabs/OAI-Processor)
- **User manual:** [OAI-Processor documentation](https://corrosionlabs.github.io/documentation/OAI-processor/)

## 3. Concept Indexer — Connect ideas

Concept Indexer is an **Obsidian community plugin** that operates on Markdown notes in a vault. It can find recurring concepts, insert wikilinks, generate master pages with contextual references, and maintain a global concept index. It also supports cross-reference analysis between concepts.

After OAI-Processor has exported conversations to Obsidian, Concept Indexer can help navigate the accumulated material by topic rather than by conversation alone.

- **Repository:** [CorrosionLabs/concept-indexer](https://github.com/CorrosionLabs/concept-indexer)
- **User manual:** [Concept Indexer documentation](https://corrosionlabs.github.io/documentation/concept-indexer-v2/)

## Getting started

1. Install and configure **OAI-Downloader**. Download the conversations and resources you want to preserve.
2. Open **OAI-Processor**, select the backup folder, analyze and process the desired projects, and export to an Obsidian vault.
3. Open that vault in **Obsidian**. Optionally install and enable **Concept Indexer**, then use it to search and index concepts across the exported notes.

Follow each application's manual for installation, configuration, requirements, and detailed usage.

## Important notes

- **Local tools:** The applications handle local backups and exported files. Concept Indexer works within your Obsidian vault.
- **Privacy:** Backups and exports may contain sensitive conversations, documents, and media. Do not publish them accidentally.
- **Independent projects:** Installing one application does not automatically install the others.
- **Platform support:** Consult the individual repositories for current operating-system support and packaged releases.
- **Not affiliated with OpenAI:** OAI Toolkit is an independent Corrosion Labs project.

## Corrosion Labs

Explore our other software: [Corrosion Labs — Tools](https://corrosionlabs.github.io/tools/).

## Support

If these tools are useful to you and you would like to support their development, visit [Corrosion Labs on Ko-fi](https://ko-fi.com/Y5Y722A4J4).
