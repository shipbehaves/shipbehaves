# Emre Yavuz · `@shipbehaves`

ships ai in places where it has to behave.

post-training across the stack: rlhf, rlvr, constitutional ai. deepest in rl and reward design, hands-on with the datasets.

[yavuz.ai](https://yavuz.ai) · [x.com/shipbehaves](https://x.com/shipbehaves) · [huggingface.co/yavuz-ai](https://huggingface.co/yavuz-ai)

---

i train, break, and measure language models and their reward signals, and write down what actually happened, nulls included.

## selected work

a few representative pieces.

- **train** · [grpo-gsm8k](https://github.com/shipbehaves/grpo-gsm8k): grpo + rlvr on gsm8k, no reward or value model. without vllm rollouts ~72s/step; with vllm colocate ~2s/step (~30x). the algorithm was never the bottleneck, the rollout was.
- **break** · [self-reward-collapse](https://github.com/shipbehaves/self-reward-collapse): does a model training on its own judgment collapse? on verifiable math, not really. a brevity signal gets reward-hacked and halves answer length, but capability holds. the honest failure was more interesting than the headline would have been.
- **measure** · [regulated-evals](https://github.com/shipbehaves/regulated-evals): regulation-anchored trustworthy-ai scorecards for frontier and open-weight models. no current model is bare-ready for regulated finance; the value is the spread, and the wrap each gap demands.
- **lifecycle** · [ai-delivery-contract](https://github.com/shipbehaves/ai-delivery-contract): an industry-neutral reference for taking ai from data to compliant production, with a runnable governance-as-code gate. the model is one component in the system; the contract around it is what gets it shipped. [interactive walkthrough →](https://shipbehaves.github.io/ai-delivery-contract/)

## open-source

- [huggingface/trl#6137](https://github.com/huggingface/trl/pull/6137): fix a `GRPOTrainer` crash on partial eval batches, with a regression test.
- [huggingface/lighteval#1271](https://github.com/huggingface/lighteval/pull/1271): fix sample-cache corruption under data-parallel, with a regression test.

## models + datasets

[huggingface.co/yavuz-ai](https://huggingface.co/yavuz-ai): trained adapters, reward models, and the preference and trajectory datasets from the work above.
