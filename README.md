# Unsatho

**A tiny transformer that trains in your browser.**

No API keys. No GPU. No install. Just one HTML file.(this readme cringe asf i made it with ai ion even wanna deal with reading it so js deal with it #fairs 👌)

[Try it here](https://drixpyyy.github.io/Unsatho/)

---

## What is this?

It's a real transformer — multi-head attention, feed-forward networks, LayerNorm, residuals, Adam optimizer, the whole thing — that trains from scratch in your browser.

When you open the page, it:

1. **Pre-trains** on raw text (learns language patterns)
2. **Fine-tunes** on Q&A pairs (learns to be a chatbot)
3. **RLHF** (learns from your feedback if you turn it on)

Then you can chat with it. It will make mistakes. That's the point.

---

## Why make this?

Big AI models are incredible, but you can't see inside them. You can't change their training data. You can't watch the loss go down.

Unsatho is the opposite. Every weight, every attention head, every gradient step is visible and tweakable.

If you've ever thought "I could build something if I just knew where to start" — this is where you start.

---

## What can I do with it?

| Thing | How |
|-------|-----|
| Change what it knows | Edit the datasets in Settings → retrain |
| Make it deeper | Increase layers / heads / d_model |
| Teach it your own facts | Add sentences to pre-training data |
| Give it a personality | Edit the Q&A pairs |
| See RLHF in action | Turn on "Live RLHF" — pick better answers, it learns |
| Save a trained model | Export to JSON, share it, import later |
| Verify it's real | Run the self-tests (Settings → Model management) |

---

## Does it actually work?

Yes. The math is correct. The gradients flow. The attention maps update in real time.

But it's tiny — about 50K-150K parameters. It will not replace ChatGPT. It will confidently tell you that "the sky is blue" and then forget what you asked three messages ago.

That's not a bug. That's the lesson.

---

## How do I use it?

1. Open the page
2. Wait 60-90 seconds while it trains
3. Type something
4. Click the **?** buttons next to any setting to see an animated explanation

**Pro tips:**
- Turn on **Reasoning mode** to see how it tokenizes your message and what tokens it's considering
- Turn on **Live RLHF** to become part of the training loop
- Turn on **Streaming** to see answers appear word by word
- Export your model before closing the tab — it won't save otherwise

---

## What's inside?

- Real multi-head causal self-attention (with backprop)
- LayerNorm + residual connections
- Feed-forward networks with GELU
- Adam optimizer with gradient clipping
- Temperature / top-K / top-P sampling
- BPETokenizer trained on your data
- Three-stage training pipeline (pretrain → SFT → RLHF)
- Export/import, self-tests, accessibility

All in one HTML file. No build step. No dependencies.

---

## Known limitations (be honest)

- **Small context window** (48-96 tokens) — it forgets quickly
- **Slow generation** (CPU only, plain JS loops)
- **Will hallucinate** — it's tiny, it guesses wrong often
- **No persistence** unless you export manually
- **Mobile works but is cramped**

These are not bugs. They're trade-offs so everything fits in one readable file.

---

## Contributing / Forking

This is meant to be remixed.

Fork the repo, open the HTML file, change whatever you want. Add a feature, break something, fix it, learn.

Ideas you could add:
- Beam search
- KV caching (speed)
- Model merging
- More sampling strategies

**Please don't ask for WebGPU.** The point is readability, not performance.

---

## License

MIT — do whatever you want. Just show someone how it works someday.

---

## Links

- [Live demo](https://drixpyyy.github.io/Unsatho/)
- [GitHub repo](https://github.com/drixpyyy/Unsatho)

---
