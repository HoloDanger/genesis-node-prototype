# 009: Six Months Later (October 2026)

*October 7, 2026*

It’s been a little over six months since I sat down to write one of these logs. Looking back at my last committed entry from March—and a draft I jotted down in May right before finals—I have to smile a bit at how intense I sounded. There was definitely some "aura farming" going on.

Back then, I think I wrote with that heavy, cinematic tone because I was trying so hard to carve out mental space. When you’re stuck in the middle of university deadlines, thesis revisions, and 37°C summer heat, wrapping your projects in grand language is almost a defense mechanism. It’s a way of telling yourself: *What I'm building matters, even if I'm currently running on four hours of sleep and coffee.*

Now that the dust has settled, I don’t feel the need to talk like an ancient cyber-monk anymore. Life looks quite different today, and I wanted to catch up and share where things actually stand.

---

### The Big Milestone: Life After Graduation

In June, I officially graduated college. 

Walking across that stage was surreal, but the real shift happened the Monday after. For the first time in years, the background hum of impending homework, exams, and academic obligations was just… gone. 

Having full ownership of your calendar is a strange feeling at first. You realize how much creative energy was being quietly drained just managing the friction of school. Once that weight was off my shoulders, the way I approached my work changed. I stopped needing to make grand philosophical declarations about technology and just started enjoying the craft of building things quietly.

---

### What Actually Got Built Over the Summer

Without the distraction of school, the projects I had been sketching out finally had room to breathe. 

Instead of jumping between different frameworks and trends, I spent the summer doubling down on simplicity:

1. **Tessera Phalanx (Our Go Retail Monolith):**  
   Earlier this year, I talked a lot about the "Potato Standard"—the idea that software should run on minimal resources without needing heavy cloud machinery. Over the summer, this turned from a nice thought into a real, functioning retail POS and ERP engine. 

   To be strict with the numbers: while the Go runtime and OS baseline put total process RSS at around **8–12 MB on Linux** and **~14 MB on macOS**, the actual **live application heap (`m.Alloc`) hovers between just 0.58 MB and 1.28 MB**. By designing the core state hashing to be strictly zero-allocation (0 allocs/op), HTTP scan-to-cart operations clock in at **29.85 microseconds**, and the entire UI (HTMX + Templ) is served directly from an 11MB binary without a single `npm` dependency. It doesn't feel like bloated enterprise software; it feels like an instant, offline physical appliance.

2. **The Genesis Overlay:**  
   I also wanted a clean, distraction-free way to interact with local AI models without having to open a heavy browser or pay for yet another monthly subscription. I put together a desktop overlay using Tauri and Ollama. It streams responses locally, boots up in less than a millisecond, and rests at around 11–18MB of RAM. It’s quiet, private, and runs entirely on device.

3. **Taming the Machine (Nix):**  
   I finally consolidated my entire environment into a single declarative Nix flake. Whether I’m on my MacBook Air or my home setup, everything—tools, compilers, editors—spins up identically with one command. No more tinkering with broken PATHs or random external runtime managers.

None of this was about proving a point to the tech industry. It was just about building a digital workspace that feels calm, responsive, and respectful of my attention.

---

### Finding a Daily Rhythm

Outside of code, the biggest change has been building a sustainable daily routine. 

When I was in school, my schedule was erratic. Nowadays, I’ve found a lot of peace in having a steady rhythm: sitting down in the morning for focused deep work, training at the gym in the afternoon (hitting some solid personal baselines on squats and deadlifts has been great for clearing my head), and spending time in the evenings studying Spanish for long-term travel plans down the road.

As we head into the last stretch of 2026, my focus is shifting toward contract work—taking these lightweight tools and my background in Go and systems architecture, and putting them to work on real-world projects.

---

### Closing Thoughts

Looking back at the journey from Post 001 to now, I think the biggest lesson has been that true peace of mind doesn't come from dramatic manifestos or cutting yourself off from the world. It comes from doing honest work, keeping things simple, and being patient with your own progress.

The forge isn’t an intense fortress anymore. It’s just my desk, a clean terminal, and a quiet space to build things that last.

I promise not to wait another six months before the next entry.
