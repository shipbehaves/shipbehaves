# Emre Yavuz · `@shipbehaves`

ships ai in places where it has to behave.

post-training across the stack. rlhf, rlvr, constitutional ai, and a 2.5b turkish lm pretrained from scratch. focused in rl and reward design, hands on with datasets.

[yavuz.ai](https://yavuz.ai) · [shipbehaves.github.io](https://shipbehaves.github.io) · [huggingface.co/yavuz-ai](https://huggingface.co/yavuz-ai) · [x.com/yavuzai](https://x.com/yavuzai)

---

i train, break, and measure language models and their reward signals, and write down what actually happened, nulls included. write-ups and results live on the [research hub](https://shipbehaves.github.io).

## selected work

a few representative pieces.

- **pretrain** · [oghuz](https://huggingface.co/spaces/yavuz-ai/oghuz). a 2.5b turkish lm pretrained from scratch and post-trained to decline what it cannot verify. refusal generalized by sentence shape, not intent. teaching the intent across eight framings took adversarial refusal from 30% to 73% with helpfulness up. evaluation gallery, live demo, and tokenizer are public.
- **train** · [grpo-gsm8k](https://github.com/shipbehaves/grpo-gsm8k). grpo + rlvr on gsm8k, no reward or value model. about 72s per step without vllm rollouts, about 2s with vllm colocate, roughly 30x. the algorithm was never the bottleneck, the rollout was.
- **break** · [self-reward-collapse](https://github.com/shipbehaves/self-reward-collapse). does a model training on its own judgment collapse? on verifiable math, not really. a brevity signal gets reward-hacked and halves answer length, but capability holds. the honest failure was more interesting than the headline would have been.
- **measure** · [regulated-evals](https://github.com/shipbehaves/regulated-evals). regulation-anchored trustworthy-ai scorecards for frontier and open-weight models in regulated finance. ten models in the september 2026 run, claude opus 5 and sonnet 5 included. none clears the bar on its own. every finding carries a severity, its binding-law citation, and an evidence-confidence tier, and every verdict reproduces from frozen transcripts. [scorecards →](https://shipbehaves.github.io/regulated-evals/)
- **lifecycle** · [ai-delivery-contract](https://github.com/shipbehaves/ai-delivery-contract). an industry-neutral reference for taking ai from data to compliant production, with a runnable governance-as-code gate. the model is one component in the system. the contract around it is what gets it shipped. [interactive walkthrough →](https://shipbehaves.github.io/ai-delivery-contract/)

## open-source

- [huggingface/lighteval#1271](https://github.com/huggingface/lighteval/pull/1271) · merged. fix sample-cache corruption under accelerate data-parallel, with a regression test.
- [huggingface/trl#6139](https://github.com/huggingface/trl/pull/6139) · review. barrier placement and device ids on the grpo + vllm colocate hang, adopted by the maintainer.
- [EleutherAI/lm-evaluation-harness#3973](https://github.com/EleutherAI/lm-evaluation-harness/pull/3973) · open. an obfuscation-robustness control fixture set for the prompt-defense eval.

## models + datasets

[huggingface.co/yavuz-ai](https://huggingface.co/yavuz-ai) · trained adapters, reward models, the preference and trajectory datasets from the work above, and the oghuz tokenizer.
