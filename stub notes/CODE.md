
2x coding speed https://github.blog/2022-09-07-research-quantifying-github-copilots-impact-on-developer-productivity-and-happiness/

## Data/Timeline

- Oct 2021: Github Copilot technical preview - [team of 6 working on it](https://twitter.com/alexgraveley/status/1607897474965839872) 
- Dec 2021: Github Copilot [for businesses](https://www.theregister.com/2022/06/21/githubs_ai_code_assistant_copilot/)
- Feb 2022: February, DeepMind introduced [AlphaCode](https://www.deeplearning.ai/the-batch/competitive-coder/), a transformer pretrained on 86 million programs in 12 programming languages and fine-tuned on entries to coding contests. At inference, it generates a million possible solutions and filters out the bad ones. In this way, it retroactively beat more than half of contestants in 10 coding competitions.
- Jun 2022: Github Copilot GA
- Sep 2022: Github Copilot [productivity survey](https://visualstudiomagazine.com/articles/2022/09/13/copilot-impact.aspx)
- Sep 2022: BigCODE https://www.servicenow.com/blogs/2022/bigcode-large-language-models.html
- Oct 2022: The Stack: 3 TB of permissively licensed source code in 30 programming languages https://huggingface.co/datasets/bigcode/the-stack
- Nov 2022: Kite.com public failure https://www.kite.com/blog/product/kite-is-saying-farewell/
  - Our diagnosis is that individual developers do not pay for tools. Their manager might, but engineering managers only want to pay for discrete new capabilities, i.e. making their developers 18% faster when writing code did not resonate strongly enough.
- Nov 2022: https://www.codeium.com/blog/beta-launch-announcement
- Dec 2022: reverse engineering copilot https://thakkarparth007.github.io/copilot-explorer/posts/copilot-internals.html#other-random-tidbits
- https://github.com/fauxpilot/fauxpilot This is an attempt to build a locally hosted version of [GitHub Copilot](https://copilot.github.com/). It uses the [SalesForce CodeGen](https://github.com/salesforce/CodeGen) models inside of NVIDIA's [Triton Inference Server](https://developer.nvidia.com/nvidia-triton-inference-server) with the [FasterTransformer backend](https://github.com/triton-inference-server/fastertransformer_backend/).
- Dec 2022: alphacode evaluation https://github.com/norvig/pytudes/blob/main/ipynb/AlphaCode.ipynb
- Jan 2023: Copilot Labs https://marketplace.visualstudio.com/items?itemName=GitHub.copilot-labs
- Feb 2023 https://www.bleepingcomputer.com/news/security/github-copilot-update-stops-ai-model-from-revealing-secrets/ Copilot will introduce a new paradigm called "Fill-In-the-Middle," which uses a library of known code suffixes and leaves a gap for the AI tool to fill, achieving better relevance and coherence with the rest of the project's code. Additionally, GitHub has updated the client of Copilot to reduce unwanted suggestions by 4.5% for improved overall code acceptance rates. "When we first launched GitHub Copilot for Individuals in June 2022, more than 27% of developers’ code files on average were generated by GitHub Copilot," Senior Director of Product Management Shuyin Zhao said.

"Today, GitHub Copilot is behind an average of 46% of a developers’ code across all programming languages—and in Java, that number jumps to 61%."

- March 2023 - more ambitious with amall scripts
	- https://simonwillison.net/2023/Mar/27/ai-enhanced-development/
	- geoffrey litt stuff
- March 2023 - Codium AI - 11m seed - https://www.codium.ai/blog/codiumai-powered-by-testgpt-accounces-beta-and-raised-11m/
- April 2023 - Replit v1 code 3b announced

## Known Issues

- Ryan Salva on how Copilot works + how to gain developer trust https://news.ycombinator.com/item?id=33226515
- https://medium.com/@enoch3712/github-copilot-is-under-the-hood-how-it-works-and-getting-the-best-out-of-it-4699d4dc3cd8
	- cushman - 2048 tokens
	- davinci - 4k tokens
- vulnerabilities https://www.spiceworks.com/it-security/security-general/news/40-of-code-produced-by-github-copilot-vulnerable-to-threats-research/
	- codex-davinci-002 [Do Users Write More Insecure Code with AI Assistants](https://arxiv.org/abs/2211.03622) some vulns found in C code with 75 participants - [media report](https://www.theregister.com/2022/12/21/ai_assistants_bad_code/)
	- codex-cushman-001 https://arxiv.org/abs/2208.09727
- Github Copilot investigation https://news.ycombinator.com/item?id=33240341
- Readers write more insecure code https://arxiv.org/abs/2211.03622 https://info.deeplearning.ai/generated-code-makes-overconfident-programmers-chinas-autonomous-drone-carrier-does-bot-therapy-require-informed-consent-mining-for-green-tech-1


## code models


- bloom bigcode https://www.servicenow.com/blogs/2022/bigcode-large-language-models.html
- salesforce codegen
- the stack from eleuther

## products

(alessio's blogpost https://evcrevolution.com/p/evc-10-llm-for-developers)

sourcegraph list https://github.com/sourcegraph/awesome-code-ai

- tensai refactor pr codegen https://twitter.com/mathemagic1an/status/1610023513334878208?s=46&t=HZzqUlCKP3qldVBoBwEzZg
- Magic https://techcrunch.com/2023/02/06/magic-dev-code-generating-startup-raises-23m/
- unmaintained
	- https://github.com/CodedotAl/gpt-code-clippy
	- https://github.com/samrawal/emacs-secondmate
- Code IDEs
	- Introducing Cursor!! ([https://cursor.so](https://t.co/wT5wRe22O2))Cursor IDE https://twitter.com/amanrsanger/status/1615539968772050946
		- why is this not a vscode extension?
	- E2b - from vasek https://github.com/e2b-dev/e2b
- the pandas extension thing - https://github.com/approximatelabs/sketch 
	- built on lambdaprompt https://github.com/approximatelabs/lambdaprompt
	- pandas dataframe chat https://github.com/gventuri/pandas-ai
	- prefectio marvin ai
- copilot labs
	- https://redmonk.com/jgovernor/2023/01/06/the-future-just-happened-developer-experience-and-ai-are-now-inextricably-linked/
- http://www.useadrenaline.com/ Show HN: Fully LLM powered code repair – fix and explain your code in seconds
- [Gptcommit: Never write a commit message again (with the help of GPT-3)](https://zura.wiki/post/never-write-a-commit-message-again-with-the-help-of-gpt-3/)
	- yet another https://news.ycombinator.com/item?id=34591733
- https://github.com/Nutlope/aicommits

- santacoder typosaurus https://twitter.com/corbtt/status/1616270918774575105?s=46&t=ZSeI0ovGBee8JBeXEe20Mg semantic linter that spots errors in code
- Buildt -  AI-powered search allows you to find code by searching for what it does, not just what it is.
	- https://twitter.com/AlistairPullen/status/1611011712345317378
- grid.io
- qqbot - dan robinson?
- YC
	- code generation - second.dev https://news.ycombinator.com/item?id=35083093
- Pygma is used to convert Figma mockups into production-ready code.
- code search
	- Phind https://news.ycombinator.com/item?id=35543668
	- bloop - AI code search https://news.ycombinator.com/item?id=34892541
	- sourcegraph cody
	stackoverflow.gg https://twitter.com/bentossell/status/1622513022781587456
- What comes after Copilot? My take: a conversation with your codebase! Introducing Tensai, your repo-level code assistant http://TensaiCode.com - jay hacks
- Tabby - Self Hosted GitHub Copilot https://news.ycombinator.com/item?id=35470915
- codecomplete - ycw23 - copilot for enterprise https://news.ycombinator.com/item?id=35152851
	- CodeComplete offers an experience similar to Copilot; we serve AI code completions as developers type in their IDEs. However, instead of sending private code snippets to GitHub or OpenAI, we use a self-hosted LLM to serve code completions. Another advantage with self-hosting is that it’s more straightforward to securely fine-tune to the company’s codebase. Copilot suggestions aren’t always tailored to a company’s coding patterns or internal libraries, so this can help make our completions more relevant and avoid adding tech debt.
- anysphere control.dev - an AI code editor that harnesses the power of GPT-4. It’s a drop-in replacement for VS Code, has context about your closed-source codebase, and it will make you 2x more productive tomorrow.
- socket.dev ai security scanning https://socket.dev/blog/introducing-socket-ai-chatgpt-powered-threat-analysis
	- https://www.theregister.com/2023/03/30/socket_chatgpt_malware/
- agent writing its own code in a loop https://github.com/pHaeusler/micro-agent
- autogenerate PRs
	- https://www.grit.io/
	- https://twitter.com/MrHunterBrooks/status/1639373651010109442?s=20
	- https://github.com/gitstart
	- AutoPR, a Github Action that autonomously writes a pull request in response to an issue https://twitter.com/IrgolicR/status/1652451501015457798


## commit msg generation

- https://github.com/di-sukharev/opencommit
- ai-commit

### Test generation

Codium - https://www.codium.ai/blog/codiumai-powered-by-testgpt-accounces-beta-and-raised-11m/
	- video demo https://twitter.com/mathemagic1an/status/1638598693623582720

###  GPT low code

- https://github.com/jbilcke/latent-browser hallucinate by MIME types 
- https://github.com/TheAppleTucker/backend-GPT backend is all you need
- https://withsutro.com/ text to app

## alternative languages

- https://github.com/jbrukh/gpt-jargon pseudolanguage
- https://github.com/eth-sri/lmql 