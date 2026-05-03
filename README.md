# build-your-own

Rebuilding real-world tools and systems from scratch in Rust, following the [Coding Challenges](https://codingchallenges.fyi/challenges/intro) series by John Crickett.

No wrapping existing binaries. No libraries that do the core work for you. Just a ground-up implementation of each thing, in Rust, until it works.

---

## Why

The best way to understand how something works is to build it yourself. Reading about how Redis handles commands or how DNS resolution works is one thing — writing it is a completely different level of understanding.

I'm using this series as deliberate practice. Each challenge is a complete, working project small enough to finish but substantial enough to actually teach you something.

---

## Challenges

| # | Challenge | Status |
|---|-----------|--------|
| 1 | [xxd](./xxd) | in progress |

This table will grow as I work through the list. Each completed challenge links to its directory.

---

## Structure

Each challenge lives in its own directory with its own `Cargo.toml`. They are fully independent — build and run any one without touching the others.

```
build-your-own/
    wc/
        src/
            main.rs
        Cargo.toml
        README.md
    json-parser/
        src/
            main.rs
        Cargo.toml
        README.md
```

Each directory has its own README covering what the real tool does, what design decisions I made, and anything interesting I ran into.

---

## Building

You need Rust. Get it from [rustup.rs](https://rustup.rs) if you don't have it.

```bash
# Build a specific challenge
cd wc
cargo build --release

# Run it
./target/release/wc somefile.txt
```

---

## Rules I set for myself

- No calling the real binary and parsing its output
- No using a library that already does the hard part
- Read the spec or man page, understand the actual behavior, then implement it
- No vibe coding — I understand every line before it gets committed
- If I get something wrong, document what I got wrong and fix it

---

## About

I'm a systems programmer working in Rust. My other projects include [Vitruvius](https://github.com/XXNOUR/Vitruvius), a decentralized P2P file sync tool with zero-knowledge encryption — built from scratch in Rust as a bachelor thesis project.

---

## License

MIT
