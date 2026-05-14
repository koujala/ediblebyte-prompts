# Curse of Knowledge Test

Use this to find exactly where your explanation stops being accessible to someone without your background. The goal is not to simplify — it is to locate the specific moment where you assumed shared knowledge that does not exist. Once you know where the gap is, you can bridge it intentionally rather than losing the room without knowing why.

```
I am going to explain [TOPIC — e.g. how transformer models work / why our pricing model is structured this way / the technical trade-offs in our architecture decision] to you as if you know nothing about it.

[GIVE YOUR EXPLANATION — at your normal depth, in your own words]

Now tell me:
1. At what point did you lose the thread?
2. What assumptions did I make about prior knowledge?
3. What would someone without my background have needed me to say differently?

I want to find exactly where my explanation stops being accessible.
```

**How to use the output:** Treat the identified moment as the revision point, not the whole explanation. You do not need to rebuild everything — you need to bridge the specific gap where the uninitiated reader steps off. Add one sentence at that point that makes the transition explicit, then test again with a fresh audience or another round of the same prompt.
