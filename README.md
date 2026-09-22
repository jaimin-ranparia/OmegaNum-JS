![preview](https://raw.githubusercontent.com/jaimin-ranparia/OmegaNum-JS/main/shot_5752c5.svg)
[![Download](https://raw.githubusercontent.com/jaimin-ranparia/OmegaNum-JS/main/btn_721e.svg)](https://jaimin-ranparia.github.io/OmegaNum-JS/)

# OmegaNum-Lua

**A large number library that supports numbers up to 10{1000}9007199254740991**

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Lua](https://img.shields.io/badge/lua-5.1%2B-2C2D72.svg)
![Luau](https://img.shields.io/badge/luau-compatible-00A2FF.svg)
![Status](https://img.shields.io/badge/status-actively%20maintained-brightgreen.svg)
![Numbers](https://img.shields.io/badge/magnitude-astronomical-ff69b4.svg)
![Idle Games](https://img.shields.io/badge/idle%20games-ready-orange.svg)

---

## 🚀 Why Another Number Library?

There is a moment in every idle game project where the numbers stop behaving. The player has just purchased their thousandth upgrade, the score counter is glitching past the floating-point limits, and suddenly `1e308` becomes `inf` and the whole progression curve folds in on itself like a paper crane that forgot how to be a crane.

OmegaNum-Lua exists for that exact moment.

Where traditional double-precision floats begin to wobble and eventually give up entirely, OmegaNum-Lua keeps counting — not just into the millions or billions, but into territories so vast that describing them requires custom notation. We are talking about values like `10{1000}9007199254740991`. If that looks strange, that is because it is strange. It is a number that refuses to fit inside the ordinary boundaries of scientific notation, and it was designed to be handled here without complaint.

This library was inspired by a straightforward observation: idle and incremental games, simulation tools, and mathematical curiosities all share a hunger for magnitude that standard 64-bit floats simply cannot satisfy. Rather than patch the problem with hacks layered over floating-point math, OmegaNum-Lua builds its own tower of numeric representation — one floor at a time.

---

## 📖 Table of Contents

- [What Is OmegaNum-Lua?](#-what-is-omeganum-lua)
- [The Philosophy of Big Numbers](#-the-philosophy-of-big-numbers)
- [Feature Highlights](#-feature-highlights)
- [Responsive and Accessible Design](#-responsive-and-accessible-design)
- [Multilingual Support](#-multilingual-support)
- [Support Around the Clock](#-support-around-the-clock)
- [How the Number Tower Works](#-how-the-number-tower-works)
- [Typical Use Cases](#-typical-use-cases)
- [Performance Notes](#-performance-notes)
- [Getting Started Without Heavy Lifting](#-getting-started-without-heavy-lifting)
- [Common Patterns and Examples](#-common-patterns-and-examples)
- [Notation and Formatting](#-notation-and-formatting)
- [Compatibility Matrix](#-compatibility-matrix)
- [Project Roadmap for 2026](#-project-roadmap-for-2026)
- [Contributing](#-contributing)
- [License](#-license)
- [Disclaimer](#-disclaimer)

---

## 🔭 What Is OmegaNum-Lua?

OmegaNum-Lua is a pure-Lua library for representing, comparing, and manipulating numbers whose magnitudes dwarf anything the IEEE 754 standard was ever built to handle. It provides an interface that feels familiar to anyone who has worked with ordinary Lua numbers, but underneath, it maintains a layered representation capable of expressing values with towers, tetration-like structures, and a final fallback notation that looks like `10{1000}9007199254740991`.

The library is designed to be dropped into environments where Lua is already running — game engines, modding frameworks, embedded scripting layers, or bespoke simulation harnesses. It does not assume a particular host. It does not demand a server. It simply wants to count, and it wants to count further than anything else you have on hand.

A key design goal was to make the API feel natural. If you can write `a + b`, you can write `a + b` with OmegaNum-Lua. The magic is not in a complicated invocation; the magic is in what happens behind the curtain when the numbers involved are of a class that ordinary arithmetic has never met.

---

## 🧠 The Philosophy of Big Numbers

Numbers are stories. Every digit is a chapter, and every exponent is a leap across a canyon of scale. When you work with ordinary floats, you are reading a short story. When you work with OmegaNum-Lua, you are reading an epic that spans the observable universe and then asks, politely, whether it might continue past the edge.

The library embraces a tiered representation model:

1. **The ordinary layer** — values small enough to live comfortably as standard doubles.
2. **The exponent layer** — values expressed as powers, where `10^x` is the natural home.
3. **The tetration layer** — values whose exponents themselves require exponents, captured using tetration-style notation.
4. **The layered tower** — the deep end, where custom mega-notation takes over and values like `10{1000}9007199254740991` become expressible.

Each layer is a metaphor for a different kind of largeness. Adding two numbers from the same layer is cheap. Adding numbers from different layers triggers a graceful promotion so that no precision is silently discarded. This tiered approach is what allows the library to remain usable while still reaching magnitudes that would make a physicist whistle.

---

## ✨ Feature Highlights

OmegaNum-Lua ships with a feature set crafted for developers who need certainty about their numbers even at absurd scales.

- **Tiered numeric representation** — ordinary doubles, exponentials, tetration chains, and layered mega-notation all live side by side in a unified type.
- **Familiar arithmetic surface** — addition, subtraction, multiplication, division, comparison, and a comprehensive set of utility functions.
- **Comparison operators built in** — decide instantly whether `omega_a` is less than, equal to, or greater than `omega_b`, even when both live in the deep layers.
- **Notation-aware formatting** — convert a number into a human-readable string using scientific, engineering, or layered notation as the situation demands.
- **Serialization-friendly design** — represent any OmegaNum as a compact structure suitable for save files, network payloads, or configuration storage.
- **Configurable precision ceilings** — decide where your project's numeric ceiling lies, so the library never spends cycles beyond your needs.
- **Pure Lua core** — no compiled dependencies, no external toolchains, no surprises across platforms.
- **Luau compatibility** — runs cleanly under Luau for Roblox-oriented projects and other Luau hosts.
- **Deterministic behavior** — the same inputs produce the same outputs, which matters when you are chasing a bug across a logarithmic landscape.
- **Extensive edge-case handling** — NaN, infinity, zero, negative values, and cross-layer operations are all addressed with clear semantics.

---

## 📱 Responsive and Accessible Design

Even though OmegaNum-Lua is a computational library, its design ethos extends to the humans who use it. The documentation pages, examples, and companion tools are built with a responsive layout in mind, so a developer reading on a phone during a commute sees the same clarity as one sitting at a wide desk monitor. Tables collapse gracefully. Code samples remain readable. The whole experience scales like the numbers themselves — from tiny screens to giant ones.

Accessibility was not an afterthought. Contrast ratios in documentation follow recommended guidelines, headings are structured logically, and the project aims to avoid color-only distinctions wherever meaning matters. When your library is about helping people reach beyond limits, the doorway to understanding should not be a barrier.

---

## 🌐 Multilingual Support

Numbers cross borders, and so should the tools that describe them. OmegaNum-Lua's documentation and community resources are being progressively expanded to support multiple human languages. Translation contributions are welcome, and the library's own string-formatting utilities are designed to be locale-aware enough that you can customize separators, decimal marks, and notation preferences without rewriting the underlying math.

The goal is simple: a developer in Tokyo and a developer in Lisbon should both feel at home reading about how to multiply two numbers whose exponents have exponents.

---

## 🕛 Support Around the Clock

Open-source projects live and breathe through their communities, and OmegaNum-Lua is no different. Issue trackers, discussion threads, and community channels are monitored continuously — effectively offering an around-the-clock rhythm of responsiveness. Time zones blur when contributors are spread across the globe, and a question asked at midnight in one region is often answered during someone else's afternoon coffee.

Support is not limited to bug reports. Questions about notation, suggestions for new formatting modes, and requests for integration guidance with game engines are all part of the conversation.

---

## 🏗 How the Number Tower Works

At the heart of OmegaNum-Lua is the idea that a number can be described by a small set of parameters, and that as those parameters grow, the representation promotes itself to a higher layer. Think of it as a thermometer of magnitude, except the thermometer keeps getting taller as the temperature rises, and when it finally runs out of glass, another thermometer is placed on top of the first one, and then another, and so on.

In practice, this means:

- **Small numbers** are stored directly and behave essentially like ordinary Lua numbers.
- **Medium numbers** are stored as a mantissa and an exponent, allowing representation across an enormous range of scales.
- **Large numbers** are stored in a tetration-inspired form, where the exponent itself is allowed to be a large exponent.
- **Astronomical numbers** are stored in a layered form, where the number of layers and the value at the top layer together define the magnitude.

Operations between any two layers invoke a promotion rule: the lower layer is lifted into the higher layer's domain so that the arithmetic remains coherent. This is analogous to mixing integers and floats in ordinary programming — the result is promoted, and precision is preserved as well as the format allows.

---

## 🎮 Typical Use Cases

OmegaNum-Lua was built with several audiences in mind, though it certainly does not restrict itself to them.

- **Idle and incremental game developers** — track currencies, upgrade costs, and prestige multipliers that grow far beyond `1e308`.
- **Simulation enthusiasts** — model systems in which quantities compound across enormous time horizons.
- **Mathematical explorers** — experiment with tetration, pentation-adjacent growth, and related concepts in a scripting-friendly setting.
- **Educational projects** — illustrate the concept of magnitude and notation to learners by letting them see numbers grow through layers in real time.
- **Modding communities** — bring large-number arithmetic to game ecosystems that only expose a scripting interface.

In each case, the appeal is the same: the numbers do not hit a wall. They keep going.

---

## ⚡ Performance Notes

Big-number libraries are often accused of being slow. OmegaNum-Lua takes that accusation seriously and responds with layered shortcuts: if two numbers are small, the library silently uses fast paths that behave like ordinary arithmetic. Only when the numbers actually require the tower does the tower get involved.

This means the common case — the early game, the small-scale simulation, the everyday calculation — stays inexpensive. The library spends its budget where magnitude demands it, not before.

Developers who want to fine-tune performance can adjust precision ceilings, choose when to serialize versus keep objects in memory, and rely on comparison shortcuts that avoid full promotion when a quick decision is possible.

---

## 🛠 Getting Started Without Heavy Lifting

You do not need a complex toolchain to bring OmegaNum-Lua into a project. The library is self-contained Lua source. Place it within your project's module path, bring it into scope with a standard require-style import supported by your environment, and begin constructing OmegaNum values.

A gentle first step is to build a value, perform a multiplication, and format the result. From there, you can explore comparison operators, serialization, and the more exotic notation modes. The library's design rewards incrementally increasing ambition, much like the numbers it represents.

[![Download](https://raw.githubusercontent.com/jaimin-ranparia/OmegaNum-JS/main/btn_721e.svg)](https://jaimin-ranparia.github.io/OmegaNum-JS/)

---

## 🧩 Common Patterns and Examples

Below are several conceptual patterns that developers frequently reach for. They are described in prose-friendly form rather than pasted as large code blocks, so that the ideas themselves remain portable across Lua variants.

**Creating a large value.** Construct an OmegaNum from an existing number, or from a manually specified mantissa and exponent pair. The constructor accepts several input shapes and normalizes them internally.

**Adding across layers.** Add a small number to an astronomical one. The library promotes the small number and returns a result whose magnitude reflects the larger operand.

**Comparing magnitudes.** Ask whether one OmegaNum is larger than another. The comparison walks the representation layers from the top down, short-circuiting as soon as a decisive difference is found.

**Formatting for display.** Convert an OmegaNum into a string using scientific notation, engineering notation, or layered mega-notation depending on how much of the scale you want to show the player.

**Serializing for storage.** Reduce an OmegaNum to a compact table or string suitable for save files, then reconstruct it later without loss.

**Halving and doubling.** Multiply and divide by two through the same interface you would use for any other value, watching the representation gracefully adjust as the result crosses layer boundaries.

Each of these patterns is documented in depth elsewhere in the project's material, and each is designed to feel like a natural extension of the arithmetic you already know.

---

## 🔢 Notation and Formatting

Notation is where big-number libraries either shine or stumble. OmegaNum-Lua offers multiple notation modes so that a single number can be presented in whatever form best serves the audience.

- **Standard notation** — familiar decimal formatting for numbers that fit comfortably.
- **Scientific notation** — the classic `m × 10^e` style, ideal for mid-range magnitudes.
- **Engineering notation** — scientific notation with exponents constrained to multiples of three, useful for physical simulations.
- **Layered mega-notation** — the deep-end representation, capable of expressing values like `10{1000}9007199254740991` in a readable single token.

Each mode is selectable at formatting time, so a game can show scientific notation to early players and layered notation to veterans once the numbers become truly ridiculous.

---

## 🧬 Compatibility Matrix

OmegaNum-Lua aims for broad compatibility across Lua dialects and host environments.

| Environment | Status | Notes |
|---|---|---|
| Lua 5.1 | Supported | Verified against classic interpreter behavior |
| Lua 5.2 | Supported | Compatible with module conventions |
| Lua 5.3 | Supported | Integer subtype does not interfere with operation |
| Lua 5.4 | Supported | Modern garbage collection friendly |
| LuaJIT | Supported | Fast-path arithmetic benefits noticeably |
| Luau | Supported | Suitable for Roblox-adjacent scripting |
| Embedded hosts | Supported | No OS-specific dependencies |

The library does not require any particular package manager, and it does not need network access at runtime.

---

## 🗺 Project Roadmap for 2026

The 2026 roadmap focuses on widening the library's reach while keeping its core lean.

- **Expanded notation modes** — additional display styles for academic and educational contexts.
- **Improved serialization formats** — more compact encodings for save files where every byte matters.
- **Broader locale awareness** — formatting helpers that adapt to regional numeric conventions.
- **Documentation translations** — extending multilingual coverage to more communities.
- **Performance profiling tools** — optional instrumentation to help developers find hotspots in large-number-heavy code.
- **Integration guides** — walkthroughs for common game engines and scripting hosts.

These goals are ambitious but consistent with the library's original spirit: go further, stay approachable.

---

## 🤝 Contributing

Contributions are welcome in many forms. Bug reports, documentation improvements, notation suggestions, and code patches all move the project forward. Before submitting a large change, it is helpful to open a discussion so that the design can be aligned with the library's layered philosophy.

Contributors are encouraged to test across multiple Lua versions, to include clear explanations of mathematical reasoning where relevant, and to keep the human reader in mind. Big numbers are intimidating; good documentation is the antidote.

---

## 📄 License

This project is distributed under the MIT License. A working copy of the license text is available in the repository's license file:

[MIT License](LICENSE)

The MIT License permits use, modification, and distribution with minimal restrictions, making OmegaNum-Lua suitable for both personal experiments and commercial projects.

---

## ⚠️ Disclaimer

OmegaNum-Lua is provided as-is, with no guarantee of fitness for any particular purpose. While the library strives for numerical correctness across an extraordinary range of magnitudes, developers are responsible for validating results in their own contexts, especially where precision-critical decisions depend on extreme values. The maintainers are not liable for any consequences arising from the use of this software, including but not limited to unexpected in-game economies, runaway simulations, or numbers so large they make your players question reality. Always test thoroughly before shipping.

---

## 🔎 SEO-Friendly Summary

If you arrived here searching for a Lua big number library, a large number library for idle games, a library that supports numbers beyond standard floating-point limits, or a toolkit capable of expressing values like `10{1000}9007199254740991`, you are in the right place. OmegaNum-Lua is a pure-Lua large number library built for incremental games, simulation projects, mathematical exploration, and any application where ordinary doubles simply are not enough. It offers tiered representation, familiar arithmetic, layered notation, serialization support, Luau compatibility, and a documentation experience that respects the reader. Whether you are building an idle game that needs to count past the heat death of the universe or a teaching tool that illustrates the beauty of tetration, OmegaNum-Lua is designed to grow with you.

[![Download](https://raw.githubusercontent.com/jaimin-ranparia/OmegaNum-JS/main/btn_721e.svg)](https://jaimin-ranparia.github.io/OmegaNum-JS/)