# AI Notes

notes on AI state of the art, with a focus on generative and large language models. These are the "raw materials" for the https://lspace.swyx.io/ newsletter.

> This repo used to be called https://github.com/sw-yx/prompt-eng, but was renamed because [Prompt Engineering is Overhyped](https://twitter.com/swyx/status/1596184757682941953).

This Readme is just the high level overview of the space; you should see the most updates in the OTHER markdown files in this repo:

- `IMAGE_GEN.md` - the most developed file, with the heaviest emphasis notes on Stable Diffusion, and some on midjourney and dalle.
	- `IMAGE_PROMPTS.md` - a small [swipe file](https://www.swyx.io/swipe-files-strategy) of good image prompts
- `TEXT.md` - text generation, mostly with GPT-4
	- `TEXT_CHAT.md` - information on ChatGPT and competitors, as well as derivative products
	- `TEXT_SEARCH.md` - information on GPT-4 enabled semantic search and other info
	- `TEXT_PROMPTS.md` - a small [swipe file](https://www.swyx.io/swipe-files-strategy) of good GPT3 prompts
- `INFRA.md` - raw notes on AI Infrastructure, Hardware and Scaling
- `AUDIO.md` - tracking audio/music/voice transcription + generation
- stub notes - very small/lightweight proto pages
  - `AGENTS.md` - tracking "agentic AI"
  - `CODE.md` - codegen models, like Copilot
  - etc...

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
<details>
<summary>Table of Contents</summary>

- [Motivational Use Cases](#motivational-use-cases)
- [Top AI Reads](#top-ai-reads)
- [Communities](#communities)
- [People](#people)
- [Misc](#misc)
- [Quotes, Reality & Demotivation](#quotes-reality--demotivation)
- [Legal, Ethics, and Privacy](#legal-ethics-and-privacy)

</details>
<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Motivational Use Cases

- images
  - https://mpost.io/best-100-stable-diffusion-prompts-the-most-beautiful-ai-text-to-image-prompts/it
  - [3D MRI synthetic brain images](https://twitter.com/Warvito/status/1570691960792580096?) - [positive reception from neuroimaging statistician](https://twitter.com/danCMDstat/status/1572312699853312000?s=20&t=x-ouUbWA5n0-PxTGZcy2iA)
  - [multiplayer stable diffusion](https://huggingface.co/spaces/huggingface-projects/stable-diffusion-multiplayer?roomid=room-0)
- video
  - img2img of famous movie scenes ([lalaland](https://twitter.com/TomLikesRobots/status/1565678995986911236))
    - [img2img transforming actor](https://twitter.com/LighthiserScott/status/1567355079228887041?s=20&t=cBH4EGPC4r0Earm-mDbOKA) with ebsynth + koe_recast
    - how ebsynth works https://twitter.com/TomLikesRobots/status/1612047103806545923?s=20
  - virtual fashion ([karenxcheng](https://twitter.com/karenxcheng/status/1564626773001719813))
  - [seamless tiling images](https://twitter.com/replicatehq/status/1568288903177859072?s=20&t=sRd3HRehPMcj1QfcOwDMKg)
  - evolution of scenes ([xander](https://twitter.com/xsteenbrugge/status/1558508866463219712))
  - outpainting https://twitter.com/orbamsterdam/status/1568200010747068417?s=21&t=rliacnWOIjJMiS37s8qCCw
  - webUI img2img collaboration https://twitter.com/_akhaliq/status/1563582621757898752
  - image to video with rotation https://twitter.com/TomLikesRobots/status/1571096804539912192
  - "prompt paint" https://twitter.com/1littlecoder/status/1572573152974372864
  - audio2video animation of your face https://twitter.com/siavashg/status/1597588865665363969
  - physical toys to 3d model + animation https://twitter.com/sergeyglkn/status/1587430510988611584
  - music videos 
    - [video killed the radio star](https://www.youtube.com/watch?v=WJaxFbdjm8c), [colab](https://colab.research.google.com/github/dmarx/video-killed-the-radio-star/blob/main/Video_Killed_The_Radio_Star_Defusion.ipynb) This uses OpenAI's Whisper speech-to-text, allowing you to take a YouTube video & create a Stable Diffusion animation prompted by the lyrics in the YouTube video
    - [Stable Diffusion Videos](https://colab.research.google.com/github/nateraw/stable-diffusion-videos/blob/main/stable_diffusion_videos.ipynb) generates videos by interpolating between prompts and audio
  - direct text2video project
    - https://twitter.com/_akhaliq/status/1575546841533497344
    - https://makeavideo.studio/ - explorer https://webvid.datasette.io/webvid/videos
    - https://phenaki.video/
    - https://github.com/THUDM/CogVideo
    - https://imagen.research.google/video/
- text-to-3d https://twitter.com/_akhaliq/status/1575541930905243652
  -  https://dreamfusion3d.github.io/
  -  open source impl: https://github.com/ashawkey/stable-dreamfusion
    - demo https://twitter.com/_akhaliq/status/1578035919403503616
-  text products
	- has a list of usecases at the end https://huyenchip.com/2023/04/11/llm-engineering.html
  - Jasper
  - GPT for Obsidian https://reasonabledeviations.com/2023/02/05/gpt-for-second-brain/
  - gpt3 email https://github.com/sw-yx/gpt3-email
  - gpt3() in google sheet [2020](https://twitter.com/pavtalk/status/1285410751092416513?s=20&t=ppZhNO_OuQmXkjHQ7dl4wg), [2022](https://twitter.com/shubroski/status/1587136794797244417) - [sheet](https://docs.google.com/spreadsheets/d/1YzeQLG_JVqHKz5z4QE9wUsYbLoVZZxbGDnj7wCf_0QQ/edit) google sheets https://twitter.com/mehran__jalali/status/1608159307513618433
	  - https://gpt3demo.com/apps/google-sheets
	  - Charm https://twitter.com/shubroski/status/1620139262925754368?s=20
  - https://www.summari.com/ Summari helps busy people read more
- market maps/landscapes
	- sequoia market map https://twitter.com/sonyatweetybird/status/1584580362339962880
	- base10 market map https://twitter.com/letsenhance_io/status/1594826383305449491
	- matt shumer market map https://twitter.com/mattshumer_/status/1620465468229451776 https://docs.google.com/document/d/1sewTBzRF087F6hFXiyeOIsGC1N4N3O7rYzijVexCgoQ/edit
	- nfx https://www.nfx.com/post/generative-ai-tech-5-layers?ref=context-by-cohere
	- a16z https://a16z.com/2023/01/19/who-owns-the-generative-ai-platform/?ref=context-by-cohere
	- madrona https://www.madrona.com/foundation-models/
- game assets - 
	- emad thread https://twitter.com/EMostaque/status/1591436813750906882
	- scenario.gg https://twitter.com/emmanuel_2m/status/1593356241283125251
	- [3d game character modeling example](https://www.traffickinggame.com/ai-assisted-graphics/)
	- MarioGPT https://arxiv.org/pdf/2302.05981.pdf https://www.slashgear.com/1199870/mariogpt-uses-ai-to-generate-endless-super-mario-levels-for-free/ https://github.com/shyamsn97/mario-gpt/blob/main/mario_gpt/level.py

## Top AI Reads

The more advanced GPT3 reads have been split out to https://github.com/sw-yx/ai-notes/blob/main/TEXT.md

- https://www.gwern.net/GPT-3#prompts-as-programming
- https://learnprompting.org/

### Beginner Reads

  - [Bill Gates on AI]([https://www.gatesnotes.com/The-Age-of-AI-Has-Begun](https://www.gatesnotes.com/The-Age-of-AI-Has-Begun)
  - [Steve Yegge on AI for developers](https://about.sourcegraph.com/blog/cheating-is-all-you-need)
  - excellent introduction to foundation models from MSR https://youtu.be/HQI6O5DlyFc
  - openAI prompt tutorial https://beta.openai.com/docs/quickstart/add-some-examples
  - google LAMDA intro https://aitestkitchen.withgoogle.com/how-lamda-works
  - DALLE2 prompt writing book http://dallery.gallery/wp-content/uploads/2022/07/The-DALL%C2%B7E-2-prompt-book-v1.02.pdf
  - https://medium.com/nerd-for-tech/prompt-engineering-the-career-of-future-2fb93f90f117
  - https://ourworldindata.org/brief-history-of-ai ai progress overview with nice charts
  - Jon Stokes' [AI Content Generation, Part 1: Machine Learning Basics](https://www.jonstokes.com/p/ai-content-generation-part-1-machine)
  - [What are transformer models and how do they work?](https://txt.cohere.ai/what-are-transformer-models/) - maybe [a bit too high level](https://news.ycombinator.com/item?id=35577138)
  - text generation
	  - humanloop's [prompt engineering 101](https://website-olo3k29b2-humanloopml.vercel.app/blog/prompt-engineering-101)
	  - Stephen Wolfram's explanations https://writings.stephenwolfram.com/2023/02/what-is-chatgpt-doing-and-why-does-it-work/
	  - https://andymatuschak.org/prompts/
	  - https://www.jonstokes.com/p/chatgpt-explained-a-guide-for-normies for normies
  - image generation
	  - https://wiki.installgentoo.com/wiki/Stable_Diffusion overview
	  - https://www.reddit.com/r/StableDiffusion/comments/x41n87/how_to_get_images_that_dont_suck_a/
	  - https://mpost.io/best-100-stable-diffusion-prompts-the-most-beautiful-ai-text-to-image-prompts/
	  - https://www.kdnuggets.com/2021/03/beginners-guide-clip-model.html 
  - for nontechnical
    - https://www.jonstokes.com/p/ai-content-generation-part-1-machine
    - https://www.protocol.com/generative-ai-startup-landscape-map
    - https://twitter.com/saranormous/status/1572791179636518913

### Intermediate Reads

  - **State of AI Report**: [2018](https://www.stateof.ai/2018), [2019](https://www.stateof.ai/2019), [2020](https://www.stateof.ai/2020), [2021](https://www.stateof.ai/2021), [2022](https://www.stateof.ai/)
  - reverse chronological major events https://bleedingedge.ai/
  - https://cims.nyu.edu/~sbowman/eightthings.pdf
	  1. LLMs predictably get more capable with increasing investment, even without targeted innovation. 
	  2. Many important LLM behaviors emerge unpredictably as a byproduct of increasing investment. 
	  3. LLMs often appear to learn and use representations of the outside world. 
	  4. There are no reliable techniques for steering the behavior of LLMs. 
	  5. Experts are not yet able to interpret the inner workings of LLMs. 
	  6. Human performance on a task isn’t an upper bound on LLM performance. 
	  7. LLMs need not express the values of their creators nor the values encoded in web text. 
	  8. Brief interactions with LLMs are often misleading.
  - openai prompt eng cookbook https://github.com/openai/openai-cookbook/blob/main/techniques_to_improve_reliability.md
  - on prompt eng overview https://lilianweng.github.io/posts/2023-03-15-prompt-engineering/
  - Recap of 2022's major AI developments https://www.deeplearning.ai/the-batch/issue-176/
  - DALLE2 asset generation + inpainting https://twitter.com/aifunhouse/status/1576202480936886273?s=20&t=5EXa1uYDPVa2SjZM-SxhCQ
  - suhail journey https://twitter.com/Suhail/status/1541276314485018625?s=20&t=X2MVKQKhDR28iz3VZEEO8w
  - composable diffusion - "AND" instead of "and" https://twitter.com/TomLikesRobots/status/1580293860902985728
  - on BPE tokenization https://towardsdatascience.com/byte-pair-encoding-subword-based-tokenization-algorithm-77828a70bee0 see also google sentencepiece and openai tiktoken
	  - source in GPT2 source https://github.com/openai/gpt-2/blob/master/src/encoder.py
	  - note that BPEs are suboptimal https://www.lesswrong.com/posts/dFbfCLZA4pejckeKc/a-mechanistic-explanation-for-solidgoldmagikarp-like-tokens?commentId=9jNdKscwEWBB4GTCQ
		  - causes math and string character issues https://news.ycombinator.com/item?id=35363769
	  - https://platform.openai.com/tokenizer and https://github.com/openai/tiktoken (more up to date: https://tiktokenizer.vercel.app/)
	  - https://observablehq.com/@simonw/gpt-3-token-encoder-decoder
  - creates its own language https://twitter.com/giannis_daras/status/1531693104821985280
  - img2img https://andys.page/posts/how-to-draw/
  - on language modeling https://lena-voita.github.io/nlp_course/language_modeling.html and approachable but technical explanation of language generation including sampling from distributions and some mechanistic intepretability (finding neuron that tracks quote state)
  - quest for photorealism https://www.reddit.com/r/StableDiffusion/comments/x9zmjd/quest_for_ultimate_photorealism_part_2_colors/
    - https://medium.com/merzazine/prompt-design-for-dall-e-photorealism-emulating-reality-6f478df6f186
  - settings tweaking https://www.reddit.com/r/StableDiffusion/comments/x3k79h/the_feeling_of_discovery_sd_is_like_a_great_proc/
    - seed selection https://www.reddit.com/r/StableDiffusion/comments/x8szj9/tutorial_seed_selection_and_the_impact_on_your/
    - minor parameter parameter difference study (steps, clamp_max, ETA, cutn_batches, etc) https://twitter.com/KyrickYoung/status/1500196286930292742
    - Generative AI: Autocomplete for everything https://noahpinion.substack.com/p/generative-ai-autocomplete-for-everything?sd=pf
    - [How does GPT Obtain its Ability? Tracing Emergent Abilities of Language Models to their Sources](https://yaofu.notion.site/How-does-GPT-Obtain-its-Ability-Tracing-Emergent-Abilities-of-Language-Models-to-their-Sources-b9a57ac0fcf74f30a1ab9e3e36fa1dc1)  good paper with the development history of the GPT family of models and how the capabilities developed


### Advanced Reads

- Transformers from scratch https://e2eml.school/transformers.html
	- transformers vs LSTM https://medium.com/analytics-vidhya/why-are-lstms-struggling-to-matchup-with-transformers-a1cc5b2557e3
	- transformer code walkthru https://twitter.com/mark_riedl/status/1555188022534176768
	- transformer familyi https://lilianweng.github.io/posts/2023-01-27-the-transformer-family-v2/
		- carmack paper list https://news.ycombinator.com/item?id=34639634
		- Transformer models: an introduction and catalog https://arxiv.org/abs/2302.07730
		- Deepmind - formal algorithms for transformers https://arxiv.org/pdf/2207.09238.pdf
	- Jay Alammar explainers
		- https://jalammar.github.io/illustrated-transformer/
		- https://jalammar.github.io/visualizing-neural-machine-translation-mechanics-of-seq2seq-models-with-attention/
- karpathy on transformers
	- **Convergence**: The ongoing consolidation in AI is incredible. When I started ~decade ago vision, speech, natural language, reinforcement learning, etc. were completely separate; You couldn't read papers across areas - the approaches were completely different, often not even ML based. In 2010s all of these areas started to transition 1) to machine learning and specifically 2) neural nets. The architectures were diverse but at least the papers started to read more similar, all of them utilizing large datasets and optimizing neural nets. But as of approx. last two years, even the neural net architectures across all areas are starting to look identical - a Transformer (definable in ~200 lines of PyTorch [https://github.com/karpathy/minGPT/blob/master/mingpt/model.py…](https://t.co/xQL5NyJkLE)), with very minor differences. Either as a strong baseline or (often) state of the art. ([tweetstorm](https://twitter.com/karpathy/status/1468370605229547522?s=20))
	- **Why Transformers won**: The Transformer is a magnificient neural network architecture because it is a general-purpose differentiable computer. It is simultaneously: 1) expressive (in the forward pass) 2) optimizable (via backpropagation+gradient descent) 3) efficient (high parallelism compute graph) [tweetstorm](https://twitter.com/karpathy/status/1582807367988654081)
	- [BabyGPT](https://twitter.com/karpathy/status/1645115622517542913) with two tokens 0/1 and context length of 3, viewing it as a finite state markov chain. It was trained on the sequence "111101111011110" for 50 iterations. The parameters and the architecture of the Transformer modifies the probabilities on the arrows.
	- Build GPT from scratch https://www.youtube.com/watch?v=kCc8FmEb1nY
	- different GPT from scratch in 60 LOC  https://jaykmody.com/blog/gpt-from-scratch/
- [137 emergent abilities of large language models](https://www.jasonwei.net/blog/emergence)
	- Emergent few-shot prompted tasks: BIG-Bench and MMLU benchmarks
	- Emergent prompting strategies
		- [Instruction-following](https://openreview.net/forum?id=gEZrGCozdqR)
		- [Scratchpad](https://openreview.net/forum?id=iedYJm92o0a)
		- [Using open-book knowledge for fact checking](https://arxiv.org/abs/2112.11446)
		- [Chain-of-thought prompting](https://arxiv.org/abs/2201.11903)
		- [Differentiable search index](https://arxiv.org/abs/2202.06991)
		- [Self-consistency](https://arxiv.org/abs/2203.11171)
		- [Leveraging explanations in prompting](https://arxiv.org/abs/2204.02329)
		- [Least-to-most prompting](https://arxiv.org/abs/2205.10625)
		- [Zero-shot chain-of-thought](https://arxiv.org/abs/2205.11916)
		- [Calibration via P(True)](https://arxiv.org/abs/2207.05221)
		- [Multilingual chain-of-thought](https://arxiv.org/abs/2210.03057)
		- [Ask-me-anything prompting](https://arxiv.org/abs/2210.02441)
  - Images
	  - Eugene Yan explanation of the Text to Image stack https://eugeneyan.com/writing/text-to-image/
	  - VQGAN/CLIP https://minimaxir.com/2021/08/vqgan-clip/
	  - 10 years of Image generation history https://zentralwerkstatt.org/blog/ten-years-of-image-synthesis
	  - Vision Transformers (ViT) Explained https://www.pinecone.io/learn/vision-transformers/
  - negative prompting https://minimaxir.com/2022/11/stable-diffusion-negative-prompt/
  - best papers of 2022 https://www.yitay.net/blog/2022-best-nlp-papers
  - [Predictability and Surprise in Large Generative Models](https://arxiv.org/pdf/2202.07785.pdf) - good survey paper of what we know about scaling and capabilities and rise of LLMs so far
- more prompt eng papers https://github.com/dair-ai/Prompt-Engineering-Guide
- https://creator.nightcafe.studio/vqgan-clip-keyword-modifier-comparison VQGAN+CLIP Keyword Modifier Comparison
- History of Transformers
	- richard socher on their contribution to attention mechanism leading up to transformers https://overcast.fm/+r1P4nKfFU/1:00:00
	- https://kipp.ly/blog/transformer-taxonomy/ This document is my running literature review for people trying to catch up on AI. It covers 22 models, 11 architectural changes, 7 post-pre-training techniques and 3 training techniques (and 5 things that are none of the above)
	- [Understanding Large Language Models A Cross-Section of the Most Relevant Literature To Get Up to Speed](https://magazine.sebastianraschka.com/p/understanding-large-language-models)
		- giving credit to Bandanau et al (2014), which I believe first proposed the concept of applying a Softmax function over token scores to compute attention, setting the stage for the original transformer by Vaswani et al (2017). https://news.ycombinator.com/item?id=35589756
	- https://finbarrtimbers.substack.com/p/five-years-of-progress-in-gpts GPT1/2/3, Megatron, Gopher, Chinchilla, PaLM, LLaMa
	- good summary paper (8 things to know) https://cims.nyu.edu/~sbowman/eightthings.pdf



We compared 126 keyword modifiers with the same prompt and initial image. These are the results.
  - https://creator.nightcafe.studio/collection/8dMYgKm1eVXG7z9pV23W
- Google released PartiPrompts as a benchmark: https://parti.research.google/ "PartiPrompts (P2) is a rich set of over 1600 prompts in English that we release as part of this work. P2 can be used to measure model capabilities across various categories and challenge aspects."
- Video tutorials
  - Pixel art https://www.youtube.com/watch?v=UvJkQPtr-8s&feature=youtu.be
- History of papers
	- 2008: Unified Architecture for NLP (Collobert-Weston) https://twitter.com/ylecun/status/1611921657802768384
	- 2015: [Semi-supervised sequence learning](https://arxiv.org/abs/1511.01432) https://twitter.com/deliprao/status/1611896130589057025?s=20
	- 2017: Transformers (Vaswani et al)
	- 2018: GPT (Radford et al)
	- 
- Misc
  - StabilityAI CIO perspective https://danieljeffries.substack.com/p/the-turning-point-for-truly-open?sd=pf
  - https://github.com/awesome-stable-diffusion/awesome-stable-diffusion
  - https://github.com/microsoft/LMOps guide to msft prompt research
  - gwern's behind the scenes discussion of Bing, GPT4, and the Microsoft-OpenAI relationship https://www.lesswrong.com/posts/jtoPawEhLNXNxvgTT/bing-chat-is-blatantly-aggressively-misaligned

### other lists like this

- https://gist.github.com/rain-1/eebd5e5eb2784feecf450324e3341c8d
- https://github.com/underlines/awesome-marketing-datascience/blob/master/awesome-ai.md#llama-models

## Communities

- StableDiffusion Discord https://discord.com/invite/stablediffusion
- LAION discord https://discord.gg/xBPBXfcFHd
- Eleuther discord: https://www.eleuther.ai/get-involved/ ([primer](https://blog.eleuther.ai/year-one/))
- https://reddit.com/r/stableDiffusion
- Akhaliq Discord: https://discord.gg/nYqfg4gnBt
- Karpathy Discord: https://discord.gg/3zy8kqD9Cp
- HuggingFace Discord: https://discuss.huggingface.co/t/join-the-hugging-face-discord/11263
- Deforum Discord https://discord.gg/upmXXsrwZc
- Lexica Discord https://discord.com/invite/bMHBjJ9wRh
- Perplexity Discord https://discord.com/invite/kWJZsxPDuX
- Chatgpt Hackers https://www.chatgpthackers.dev/
- Agents
	- AutoGPT discord
	- BabyAGI discord
- Midjourney's discord
  - how to use midjourney v4 https://twitter.com/fabianstelzer/status/1588856386540417024?s=20&t=PlgLuGAEEds9HwfegVRrpg
- https://stablehorde.net/


## People

This list will be out of date but will get you started. My live list of people to follow is at: https://twitter.com/i/lists/1585430245762441216

- Researchers/Developers
  - https://twitter.com/_jasonwei
  - https://twitter.com/johnowhitaker/status/1565710033463156739
  - https://twitter.com/altryne/status/1564671546341425157
  - https://twitter.com/SchmidhuberAI
  - https://twitter.com/nearcyan
  - https://twitter.com/karinanguyen_
  - https://twitter.com/abhi_venigalla
  - https://twitter.com/advadnoun
  - https://twitter.com/polynoamial
  - https://twitter.com/vovahimself
  - https://twitter.com/sarahookr
  - https://twitter.com/shaneguML
  - https://twitter.com/MaartenSap
  - https://twitter.com/ethanCaballero
  - https://twitter.com/ShayneRedford
  - https://twitter.com/seb_ruder
  - https://twitter.com/rasbt
  - https://twitter.com/wightmanr
  - https://twitter.com/GaryMarcus
  - https://twitter.com/ylecun
  - https://twitter.com/karpathy
  - https://twitter.com/pirroh
  - https://twitter.com/eerac
- News/Aggregators
  - https://twitter.com/ai__pub
  - https://twitter.com/WeirdStableAI
  - https://twitter.com/multimodalart
  - https://twitter.com/LastWeekinAI
  - https://twitter.com/paperswithcode
  - https://twitter.com/DeepLearningAI_
  - https://twitter.com/dl_weekly
  - https://twitter.com/slashML
  - https://twitter.com/_akhaliq
  - https://twitter.com/aaditya_ai
  - https://twitter.com/bentossell
  - https://twitter.com/johnvmcdonnell
- Founders/Builders/VCs
  - https://twitter.com/levelsio
  - https://twitter.com/goodside
  - https://twitter.com/c_valenzuelab
  - https://twitter.com/Raza_Habib496
  - https://twitter.com/sharifshameem/status/1562455690714775552
  - https://twitter.com/genekogan/status/1555184488606564353
  - https://twitter.com/levelsio/status/1566069427501764613?s=20&t=camPsWtMHdSSEHqWd0K7Ig
  - https://twitter.com/amanrsanger
  - https://twitter.com/ctjlewis
  - https://twitter.com/sarahcat21
  - https://twitter.com/jackclarkSF
  - https://twitter.com/alexandr_wang
  - https://twitter.com/rameerez
  - https://twitter.com/scottastevenson
  - https://twitter.com/denisyarats
- Stability
  - https://twitter.com/StabilityAI
  - https://twitter.com/StableDiffusion
  - https://twitter.com/hardmaru
  - https://twitter.com/JJitsev
- OpenAI
  - https://twitter.com/sama
  - https://twitter.com/ilyasut
  - https://twitter.com/miramurati
- HuggingFace
  - https://twitter.com/younesbelkada
- Artists
  - https://twitter.com/karenxcheng/status/1564626773001719813
  - https://twitter.com/TomLikesRobots
- Other 
  - Companies
    - https://twitter.com/AnthropicAI
    - https://twitter.com/AssemblyAI
    - https://twitter.com/CohereAI
    - https://twitter.com/MosaicML
    - https://twitter.com/MetaAI
    - https://twitter.com/DeepMind
    - https://twitter.com/HelloPaperspace
- Bots and Apps
  - https://twitter.com/dreamtweetapp
  - https://twitter.com/aiarteveryhour


## Quotes, Reality & Demotivation

- Narrow, tedium domain usecases https://twitter.com/WillManidis/status/1584900092615528448 and https://twitter.com/WillManidis/status/1584900100480192516
- antihype https://twitter.com/alexandr_wang/status/1573302977418387457
- antihype https://twitter.com/fchollet/status/1612142423425138688?s=46&t=pLCNW9pF-co4bn08QQVaUg
- prompt eng memes
	- https://twitter.com/_jasonwei/status/1516844920367054848
- things stablediffusion struggles with https://opguides.info/posts/aiartpanic/
- New Google
  -  https://twitter.com/alexandr_wang/status/1585022891594510336
-  New Powerpoint
  -  via emad
-  Appending prompts by default in UI
  -  DALLE: https://twitter.com/levelsio/status/1588588688115912705?s=20&t=0ojpGmH9k6MiEDyVG2I6gg
- There have been two previous winters, one 1974-1980 and one 1987-1993. https://www.erichgrunewald.com/posts/the-prospect-of-an-ai-winter/



## Legal, Ethics, and Privacy

- NSFW filter https://vickiboykis.com/2022/11/18/some-notes-on-the-stable-diffusion-safety-filter/
- On "AI Art Panic" https://opguides.info/posts/aiartpanic/
- Yannick influencing OPENRAIL-M https://www.youtube.com/watch?v=W5M-dvzpzSQ
- art schools accepting AI art https://twitter.com/DaveRogenmoser/status/1597746558145265664
- DRM issues https://undeleted.ronsor.com/voice.ai-gpl-violations-with-a-side-of-drm/
- stealing art [https://stablediffusionlitigation.com](https://stablediffusionlitigation.com/)
	- http://www.stablediffusionfrivolous.com/
	- stable attribution https://news.ycombinator.com/item?id=34670136
	- coutner argument for disney https://twitter.com/jonst0kes/status/1616219435492163584?s=46&t=HqQqDH1yEwhWUSQxYTmF8w
	- research on stable diffusion copying https://twitter.com/officialzhvng/status/1620535905298817024?s=20&t=NC-nW7pfDa8nyRD08Lx1Nw This paper used Stable Diffusion to generate 175 million images over 350,000 prompts and only found 109 near copies of training data. Am I right that my main takeaway from this is how good Stable Diffusion is at *not* memorizing training examples?

## Alignment, Safety

- Anthropic - https://arxiv.org/pdf/2112.00861.pdf
	- Helpful: attempt to do what is ask. concise, efficient. ask followups. redirect bad questions.
	- Honest: give accurate information, express uncertainty. don't imitate responses expected from an expert if it doesn't have the capabilities/knowledge
	- Harmless: not offensive/discriminatory. refuse to assist dangerous acts. recognize when providing sensitive/consequential advice
	- criticism and boundaries as future direction https://twitter.com/davidad/status/1628489924235206657?s=46&t=TPVwcoqO8qkc7MuaWiNcnw
- Just Eliezer entire body of work
	- https://twitter.com/esyudkowsky/status/1625922986590212096
	- agi list of lethalities https://www.lesswrong.com/posts/uMQ3cqWDPHhjtiesc/agi-ruin-a-list-of-lethalities
	- note that eliezer has made controversial comments [in the past](https://twitter.com/johnnysands42/status/1641349759754485760?s=46&t=90xQ8sGy63D2OtiaoGJuww) and also in [recent times](https://twitter.com/lorakolodny/status/1641448759086415875?s=46&t=90xQ8sGy63D2OtiaoGJuww) ([TIME article](https://time.com/6266923/ai-eliezer-yudkowsky-open-letter-not-enough/))
- Connor Leahy may be a more sane/measured/technically competent version of yud https://overcast.fm/+aYlOEqTJ0
	- it's not just paperclip factories
	- https://www.lesswrong.com/posts/HBxe6wdjxK239zajf/what-failure-looks-like
- the 6 month pause letter
	- https://futureoflife.org/open-letter/pause-giant-ai-experiments/
	- yann lecun vs andrew ng https://www.youtube.com/watch?v=BY9KV8uCtj4
	- https://scottaaronson.blog/?p=7174
	- [emily bender response](https://twitter.com/emilymbender/status/1640920936600997889)
	- [Geoffrey Hinton leaving Google](https://news.ycombinator.com/item?id=35771104) 

### regulation

- chinese regulation https://www.chinalawtranslate.com/en/overview-of-draft-measures-on-generative-ai/
	- https://twitter.com/mmitchell_ai/status/1647697067006111745?s=46&t=90xQ8sGy63D2OtiaoGJuww
- italy banning chatgpt

## Misc

- Whisper
  - https://huggingface.co/spaces/sensahin/YouWhisper YouWhisper converts Youtube videos to text using openai/whisper.
  - https://twitter.com/jeffistyping/status/1573145140205846528 youtube whipserer
  - multilingual subtitles https://twitter.com/1littlecoder/status/1573030143848722433
  - video subtitles https://twitter.com/m1guelpf/status/1574929980207034375
  - you can join whisper to stable diffusion for reasons https://twitter.com/fffiloni/status/1573733520765247488/photo/1
  - known problems https://twitter.com/lunixbochs/status/1574848899897884672 (edge case with catastrophic failures)
- textually guided audio https://twitter.com/FelixKreuk/status/1575846953333579776
- Codegen
  - CodegeeX https://twitter.com/thukeg/status/1572218413694726144
  - https://github.com/salesforce/CodeGen https://joel.tools/codegen/
- pdf to structured data - Impira used t to do it (dead link: https://www.impira.com/blog/hey-machine-whats-my-invoice-total) but if you look hard enough on twitter there are some alternatives
- text to Human Motion diffusion https://twitter.com/GuyTvt/status/1577947409551851520
  - abs: https://arxiv.org/abs/2209.14916 
  - project page: https://guytevet.github.io/mdm-page/
