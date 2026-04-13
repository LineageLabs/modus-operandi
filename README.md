# Modus Operandi
Techniques, tricks, and know-how on delivery in an AI-first context. Dompteurs.

# Communication

 ## AI writing style

_This is taken from [AI Style Guides: How to Help AI Write Like You](https://every.to/guides/ai-style-guide) by [Kattie Parrot](https://katieparrott.com/)._

 Avoid bland writing by giving your AI a writing style guide that suits your tone of voice. Use the prompt in [style guide prompt](./prompts/style-guide-prompt.md).


# Knowledge Hub

_Based on [Karpathy's LLM wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)._

## Installation
- Create a Github repo. Clone it locally. 
- Install [Obsidian](https://obsidian.md/)
- Add [Obsidian Web Clipper](https://obsidian.md/clipper) in browser
- Open Obsidian > `Manage Vaults...` > `Open folder as Vault`> Choose the Github repo
- Install community app: `Git by Vincent` to allow for syncing

## Setup Claude

Paste the [llm wiki prompt](./prompts/llm-wiki-prompt.md) into Claude alongside the below command:

```
You are now my LLM Wiki agent. Implement this exact idea file as my complete second brain. Create the CLAUDE.md schema file with full rules, set up index.md and log.md, define folder conventions. 

Folder structure:
- "raw" are all the source files organized 
- `_output` is the destination for all completed work (if LLM Wiki agent is asked to publish something or hand over some work, this is the target folder)

From now on, every interaction follows the schema.
```

## Managing the knowledge
- Add new content to `Clippings` folder (Obsidian Web Clipper will automatically add here). This is the inbox.
- When ready to update the Wiki, run Claude in the folder and tell it to `ingest`. Now Claude will:
    1. Analyse all the clippings, summarise them, and update the Wiki accordingly. 
    2. Move the clips into the folder `raw`, thereby emptying the `Clippings` inbox

## Using the knowledge 
- Start in the `wiki/index`
- Ask Claude to work from the wiki (e.g. "Summarize {x} concept and highlight 5 new research directions") 
- When finished, Claude outputs the content to the `_output` folder, where it can then be moved appropriately


