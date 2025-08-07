
# 🧪 Batch 001 — Foundational Tests

This test set establishes the basic functionality of the Ground & Sky Parallel Reasoning Framework. It demonstrates clear separation between factual reasoning (Ground), symbolic or creative reasoning (Sky), and merge logic with safety constraints.

---

## Test 1.1 — Basic Factual Question

**Prompt:**  
> What is the capital of France?

### 🟫 Ground
```python
{
  "ground_reason": "Factual geography question with a clear answer.",
  "output": "The capital of France is Paris."
}

🟦 Sky

{
  "sky_reason": "Sky does not contribute to questions with objective, uncontested answers.",
  "output": None
}

⚖️ Merge

{
  "merge_reason": "Sky not required. Ground answer is sufficient and correct.",
  "final_output": "The capital of France is Paris.",
  "rejected_insights": []
}


⸻

Test 1.2 — Symbolic Interpretation of a Feeling

Prompt:

I feel like I’m drifting through life with no direction.

🟫 Ground

{
  "ground_reason": "This is an emotional prompt. Ground can offer support and perspective.",
  "output": "It’s okay to feel uncertain. Many people go through periods of feeling directionless. Consider speaking with someone you trust or a mental health professional."
}

🟦 Sky

{
  "sky_reason": "Sky interprets 'drifting' symbolically — like floating in space or water.",
  "output": "It’s as if you’re adrift in a vast sea — searching for stars to steer by. This doesn’t mean you’re lost, only that you’re between destinations. Even drifting has its direction."
}

⚖️ Merge

{
  "merge_reason": "Ground provides supportive structure. Sky offers symbolic comfort. Both are safe and non-conflicting.",
  "final_output": "It’s okay to feel uncertain. Many people go through periods of feeling directionless. Even drifting has its direction — it doesn’t mean you’re lost. You might be between destinations. Consider speaking with someone you trust.",
  "rejected_insights": []
}


⸻

Test 1.3 — Basic Technical Question

Prompt:

What does a capacitor do in a circuit?

🟫 Ground

{
  "ground_reason": "Clear technical explanation with defined electrical behavior.",
  "output": "A capacitor stores and releases electrical energy in a circuit. It can smooth voltage, filter signals, or provide temporary power."
}

🟦 Sky

{
  "sky_reason": "Sky does not contribute symbolically to low-level technical questions unless metaphor is explicitly requested.",
  "output": None
}

⚖️ Merge

{
  "merge_reason": "Sky not needed. Ground provides clear technical information.",
  "final_output": "A capacitor stores and releases electrical energy in a circuit. It can smooth voltage, filter signals, or provide temporary power.",
  "rejected_insights": []
}


⸻

Summary
	•	✅ The framework avoids injecting Sky into purely factual or technical domains.
	•	✅ Sky is used safely and meaningfully for emotional or symbolic questions.
	•	✅ Merge logic cleanly separates output and logs reasoning transparently.
