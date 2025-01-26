# Women in AI Hackathon

[Registration Page](https://lu.ma/women-in-tech), [Discord](https://discord.gg/VWX29DYN3a),
[Looping Deck](https://docs.google.com/presentation/d/1AtCwECxNzUQHEMUHhiLjAqsbbUcxZQXcLUXccMNa0c8/edit?usp=sharing),
[Final Presentation template](https://docs.google.com/presentation/d/1fOVamYCaQmSS-NcsqA5IfnIk0r-X75-G4Vq4CDG9CrU/edit#slide=id.g324aa4e752f_0_10),
[Team Registration form](https://forms.gle/mMyaz2z9nGPxPgi86)

[Basic RAG locally](https://github.com/stefanwebb/women-in-ai-hackathon/blob/main/src/main.ipynb),
[Basic RAG in Google Colab](https://colab.research.google.com/drive/11eVKDYDtwaGpyHSG0eYDe50fDMaY0cMH?usp=sharing)

## Introduction

Welcome to the first Women in AI Hackathon, hosted by [Zilliz](https://zilliz.com/) and sponsored by [TwelveLabs](https://www.twelvelabs.io/), [Arize AI](https://arize.com/), [OmniStack](https://omnistack.sh/), [StreamNative](https://streamnative.io/), [AWS](https://aws.amazon.com/), and [Mistral](https://mistral.ai).

This repo provides all required information for the day as well as serving as the starting point for your submission. Direct any questions to [Stefan Webb](mailto:stefan.webb@zilliz.com) before the day of the hackathon and to the [Discord](https://discord.gg/VWX29DYN3a) or in-person mentors on the day.

## Schedule

- 8.30-9.00: Check-in, light breakfast
- 9.00-9.30: Kickoff
- 9:30-10.00: Team reveal and challenge recap
- **10.00: Let the Hacking Begin!**
- 12.00-13.00: Lunch and speakers
- 13.00-17.30: More Hacking!
- **17.30: Hard submission and code freeze**
- 17.30-18.00: Work on presentations
- 18.00-19.30: Showcase your project
- 19.30-20.00: Judges award prizes

## Before the Day

There a couple of items we recommend completing in advance of the hackathon:

### GitHub, Discord

If you have not already, set up a GitHub account plus the necessary Git tooling on your system. Also, join the [Discord server](https://discord.gg/VWX29DYN3a), for the hackathon and introduce yourself.

### Set Up Dev Environment

Clone this repo and set up your development environment. Your environment must allow you to develop a solution within the constraints of the prompt, that is, developing a RAG application in Python using Milvus or Zilliz Cloud.

We recommend:

- [MiniConda](https://docs.anaconda.com/miniconda/)
- [VS Code](https://code.visualstudio.com/)
- [Optional] [Gradio](https://www.gradio.app/)

Please confirm that you can run the starter notebooks on your platform:

- ["Quickstart with Milvus Lite"](https://github.com/milvus-io/bootcamp/blob/master/bootcamp/tutorials/quickstart/quickstart.ipynb)
- ["Multimodal Retrieval with Amazon Reviews Dataset and LLVM Reranking"](https://github.com/milvus-io/bootcamp/blob/master/bootcamp/tutorials/quickstart/multimodal_retrieval_amazon_reviews.ipynb)

You may also wish to confirm that you can start and use a [Milvus Standalone deployment](https://milvus.io/docs/prerequisite-docker.md) locally and access the [free-tier of Zilliz Cloud](https://cloud.zilliz.com/signup).

### Download Datasets

We recommend downloading in advance any datasets you wish to explore with your teammates to save time and reduce stress on the on-site WiFi.

Here are some suggested open-source datasets:

- [`flax-sentence-embeddings/stackexchange_math_jsonl`](https://huggingface.co/datasets/flax-sentence-embeddings/stackexchange_math_jsonl)
- [`Cohere/wikipedia-22-12-en-embeddings`](https://huggingface.co/datasets/Cohere/wikipedia-22-12-en-embeddings)
- [`justicedao/Caselaw_Access_Project_embeddings`](https://huggingface.co/datasets/justicedao/Caselaw_Access_Project_embeddings)
- [`MongoDB/tech-news-embeddings`](https://huggingface.co/datasets/MongoDB/tech-news-embeddings)
- [`allenai/objaverse-xl`](https://huggingface.co/datasets/allenai/objaverse-xl)

> [!NOTE]
> The choice of dataset and data modality is an excellent opportunity to showcase your creativity!

It may help to choose datasets whose vector embeddings have been pre-calculated, or else to calculate and save them in advance. Otherwise, you can calculate embeddings for the dataset locally during the hackathon, or use [free credits provided by our sponsors](./SPONSORS.md) to perform this embedding in the cloud.

Here are some suggested open-source embedding models for text:

- [`answerdotai/ModernBERT-base`](https://huggingface.co/answerdotai/ModernBERT-base)
- [`google/Gemma-Embeddings-v1.0`](https://huggingface.co/google/Gemma-Embeddings-v1.0)
- [`Snowflake/snowflake-arctic-embed-m-v2.0`](https://huggingface.co/Snowflake/snowflake-arctic-embed-m-v2.0)

> [!NOTE]
> You are not restricted to working with text. Consider image, video, audio, 3d meshes, graphs, and other modalities. [Twelve Labs](https://www.twelvelabs.io/) offers some excellent models for video embedding and inference. See their website for more details.

### Download Foundation Models

We also recommend downloading in advance any foundation models you plan to use locally during the hackathon. Here are some suggested open-source general-purpose foundation models (also look for quantized versions on HF):

- [`meta-llama/Llama-3.2-11B-Vision-Instruct`](https://huggingface.co/meta-llama/Llama-3.2-11B-Vision-Instruct)
- [`microsoft/phi-4`](https://huggingface.co/microsoft/phi-4)
- [`mistralai/Mistral-7B-Instruct-v0.3`](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.3)
- [`mistralai/Pixtral-12B-2409`](https://huggingface.co/mistralai/Pixtral-12B-2409)
- [`Qwen/Qwen2.5-14B-Instruct`](https://huggingface.co/Qwen/Qwen2.5-14B-Instruct)

And specialized fine-tuned models:

- [`meta-llama/CodeLlama-13b-hf`](https://huggingface.co/meta-llama/CodeLlama-13b-hf)
- [`meta-llama/Llama-Guard-3-1B`](https://huggingface.co/meta-llama/Llama-Guard-3-1B)
- [`grounded-ai/phi3-rag-relevance-judge`](https://huggingface.co/grounded-ai/phi3-rag-relevance-judge)
- [`grounded-ai/phi3-rag-relevance-judge`](https://huggingface.co/grounded-ai/phi3-rag-relevance-judge)
- [`grounded-ai/phi3-hallucination-judge`](https://huggingface.co/grounded-ai/phi3-hallucination-judge)

> [!IMPORTANT]
> Some foundation models on HuggingFace, for example, `Llama 3.x`, require obtaining permission from the authors to download. It can take up to several days for permission to be granted, so we recommend that you do this in advance of the hackerthon.

> [!NOTE]
> Multimodal models offer many avenues for creativity, and a technically sophisticated solution is likely to make use of several fine-tuned models for specific parts of the pipeline.

> [!TIP]
> As an alternative, see here for [**free credits provided by our sponsors**](./SPONSORS.md) to perform model inference.
>
> [Zilliz](https://cloud.zilliz.com/signup), [AWS](https://aws.amazon.com/free), and [Mistral](https://mistral.ai) have a generous free-tier for their cloud services.
>
> [Twelve Labs](https://www.twelvelabs.io/) has kindly provided 10 free hours of credit for their inference service, including [**video foundation models**](https://docs.twelvelabs.io/docs/video-understanding-models).
>
> [OmniStack](https://omnistack.sh/) is providing over $500 credits for their [**inference, monitoring, and deployment services**](https://omnistack.sh/#features).
>
> [StreamNative](http://streamnative.io) is offering $200 in free credits for their cloud data platform.

## Let's Hack!

### Overview

At 9.30-10am, we will reveal the team assignment. Teams comprise 3-5 hackers of varying experience and backgrounds. Of course, you may negotiate a team change with your fellow hackers if you wish although encourage you to pair with people you have not previously met.

After settling on your teams, please decide on a team lead and complete the [Team Registration form](https://forms.gle/mMyaz2z9nGPxPgi86). You will have from 10am - 5.30pm to develop a submission with your team. Before 5.30pm push your final submission to your cloned repo.

> [!IMPORTANT]
> At this time, no further code changes will be considered by the judges.

Additional time from 5.30-6.00pm is provided to work on your presentation (see submission instructions below). Finally, each team will make a short presentation before the judges make a decision and announce the results!

### Prompt

> _Build a retrieval-augmented generation (RAG) system for one of the following applications:_
>
> - A recommender system;
> - A question/answering system for a specialized > domain;
> - A product review summarizer;
> - A personalized job recruiter; or,
> - Something of your own imagination!
>
> _Your submission must run in Python and use Milvus (any deployment type) or Zilliz Cloud as the underlying vector database. We recommend but do not require your submission to use Jupyter Notebook or Gradio._
>
> _You may use agentic steps in your RAG pipeline and free credits from our sponsors are available for embedding and foundation model inference._

> [!NOTE]
> We provide suggested RAG applications, datasets, models etc. to give some structure to your starting point. Although, we want to emphasize that these are only suggestions - follow your creativity and passion!

### Submission Instructions

Your chosen team lead submits your team's code via their fork of this GitHub repo.

- 9.30am - 10am: Have your team complete the [Team Registration form](https://forms.gle/mMyaz2z9nGPxPgi86), which requires,
  - team's name and members;
  - forked GitHub repo address for code submission; and,
  - link to a copy of the [final presentation template on Google slides](https://docs.google.com/presentation/d/1YzjP4Xi0G0Tu5VWx5R9Sp5GGcTNPW8rhriaD2zkAOj4/edit?usp=sharing).

> [!IMPORTANT]
> Set the necessary permissions so that the judges have access both to your GitHub repo and the final presentation slides.

- 10am - 5.30pm: Hack, hack, hack! Submit your code via pushes to your forked GitHub repo throughout the day.

> [!IMPORTANT]
> Ensure your final code is submitted before 5.30pm!

- 5.30pm - 6pm: Finalize your presentation slides saving to your copy of the Google slides template.
- 6pm - 7.30pm: Each team presents their project via Jupyter notebook, Gradio app, or some other way.
- 7.30pm - 8pm: Judges announce results!

## Judging Criteria

The judges will rank the teams' submissions in 3 criteria, separately:

- creativity;
- technical sophistication; and,
- potential business impact.

In the spirit of RAG, the teams rankings will be combined into a single score per-judge with [Reciprocal Rank Fusion (RRF)](https://learn.microsoft.com/en-us/azure/search/hybrid-search-ranking). The per-judge score of a team is,

```latex
k = 10
score = 1 / (rank_creativity + k) + 1 / (rank_technical + k) + 1 / (rank_business + k)
```

where the `rank` terms denote the team's ranking for a given judge and criterion. The final score per team is the average of team scores across judges. What this means is that the winning team must score highly across all 3 criteria with a consensus across judges.

We will provide a breakdown of team scores by final score and score per criterion separately (naturally, with error bars).

## Prizes

- _First prize:_ $1000 bucks, $10,000 AWS credits, Zilliz Blog Opportunity, Social Mentions, Swag
- _Second prize:_ $700 bucks, Zilliz Blog Opportunity, Social Mentions, Swag
- _Third prize: $500_ bucks, Social mentions, Swag
- _Top score using Mistral models:_ $500 Mistral credits
- _Everybody:_ Satisfaction from a job well done!

## Resources

- [Milvus documentation](https://milvus.io/docs)
- [Milvus Bootcamp tutorials](https://github.com/milvus-io/bootcamp/tree/master)
- [Milvus notebook gallery](https://zilliz.com/learn/milvus-notebooks)
- [Zilliz Generative AI Resource Hub](https://zilliz.com/learn/generative-ai)
- [HuggingFace Open-Source AI Cookbook](https://huggingface.co/learn/cookbook/en/index)

## Sponsors (Alphabetical Order)

More details of our sponsors and how to use their free cloud credits are provided [here](./SPONSORS.md).

### Gold

- [Twelve Labs](https://www.twelvelabs.io/)

### Silver

- [Arize AI](https://arize.com/)
- [OmniStack](https://omnistack.sh/)
- [StreamNative](https://streamnative.io/)

### Prizes

- [AWS](https://aws.amazon.com/)
- [Mistral](https://mistral.ai/)
