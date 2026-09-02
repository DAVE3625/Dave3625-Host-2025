# Dave3625 - Lab 8

## Running a Norwegian LLM

**Start here: [Dave3625_NoraLLM.ipynb](./Dave3625_NoraLLM.ipynb)**

Running [NorMistral-7b-warm-instruct](https://huggingface.co/norallm/normistral-7b-warm-instruct), a Norwegian instruction-tuned language model. The notebook covers chatting with the model without history, then with conversation history, and finishes with a quick text-to-image example using Stable Diffusion.

> The notebook and its prompts are in Norwegian.

## ⚠️ This lab does not use UV

**Unlike every other lab, you cannot run this one locally.** It needs a GPU and downloads a 7-billion-parameter model, so there is no `uv init` step here.

Run it in Google Colab instead:

1. Go to [colab.research.google.com](https://colab.research.google.com/).
2. Upload `Dave3625_NoraLLM.ipynb` (**File → Upload notebook**).
3. Switch the runtime to a GPU: **Runtime → Change runtime type → T4 GPU**. Do this *before* running any cells.
4. Run the cells from the top. The first one installs `bitsandbytes` and `accelerate`; loading the model then takes a few minutes.

If you skip step 3 the model will fail to load — that is the most common problem with this lab.


*Authors: Bjarki Thor Norddahl, Victoria Kolsing, Magnus Kristian Wiik*

New to the repo? See [Help/navigating-the-repo.md](../Help/navigating-the-repo.md).
