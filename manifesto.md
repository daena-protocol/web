# The Daena Manifesto

I want to be done with websites.

Not the internet. Websites. The thing where I open a tab, scroll past a cookie banner, dismiss a chatbot, close a popup, hunt through a hamburger menu, and finally find — maybe — the answer to a question I could have asked in five words.

The internet is good. The internet has been ruined.

Three things, that's all I want:

  1. Let me ask a question.
  2. Give me a correct answer.
  3. No hallucinations.

The strange thing is, the technology to do this already exists. The reason it doesn't happen is that the entire web was designed around the wrong unit. The website is a *visual* artifact, a thing for human eyes to scan. Computers — including the AI agents that now act for us — have to scrape, parse, and infer to extract anything useful from it. Half the time they get it wrong. The rest of the time, you didn't actually need a 200ms page render — you needed three lines of structured data.

The fix is not a better website. The fix is a second layer.

## A web with two layers

Picture the internet as it works today: humans browse, agents scrape. One pipe, built for eyes, with software cosplaying as a human to read it.

Now picture it with two layers.

The **agent layer** is canonical. Every publisher exposes a structured, signed, cryptographically verifiable source of truth — their facts, their capabilities, their hours, their prices. Agents read it directly. No HTML in the loop. No hallucination, because every fact carries a signature from the publisher.

The **human layer** is derived. When a person wants to look at the data themselves, a renderer turns it into a clean, readable page — automatically. The publisher doesn't hand-code a website. The site is just one of many views of the same data.

The same document, two interfaces. Humans don't lose their web; they get a better one — because it's generated from structured truth instead of typeset by some company's marketing team.

In Avestan, *daena* means *one's truthful self, made visible*. That is what every publisher commits to when they join: their facts, attested with their key, accountable to their identity.

## Asha and Druj

The old Persians had two words for the order of the world.

*Asha* is truth — not a moral preference, but a structural property. The universe is ordered by Asha; reality and accuracy are the same thing.

*Druj* is the lie — the disorder that distorts what is real.

The current web is full of Druj. Hallucinated facts. Stale prices. Manipulative summaries. Paid placements masquerading as recommendations. Pages that obey a publisher's intent more than the user's question. The agents we deploy on top of all this inherit it.

Daena is a protocol that puts Asha back. Every fact is cryptographically attested. Every modification breaks the signature. Every agent that trusts a Daena document does so on math, not vibes. The structure of the system makes Druj harder than Asha — for the first time in the internet's history.

## What it is, concretely

Daena Protocol v0 is a small, sharp specification with a complete reference implementation in TypeScript:

- A document format: facts, capabilities, render hints, signature — all in JSON.
- A signing layer: ed25519 over canonicalized content, verifiable against the publisher's DID.
- A consumer surface for agents: fetch, verify, query, act — verified by default.
- A renderer that turns the same document into a human web page when needed.

Publishers can scaffold, sign, validate, and ship a document in four commands. Agents can read it with one. The protocol is open, permissively licensed, and lives in public at [github.com/daena-protocol](https://github.com/daena-protocol).

It is pre-alpha. The spec will move. The packages will rev. Anyone who shows up early helps shape what v1 looks like.

## The call

If you **publish things** — a restaurant, a clinic, a library, a city services portal, a documentation site, a product catalog — try Daena. Sign your data. Be a verifiable source.

If you **build agents** — chat assistants, research tools, browsing copilots, any software that acts on a person's behalf — try Daena. Read from verifiable sources. Stop guessing what some HTML page meant.

If you **build infrastructure** — content management, search, payments, identity — help define the rails. Open a discussion, file a DPIP, ship a connector.

If you just **hate how the web works** — share this. Talk about it. The internet is good. We can make it good again.

---

The protocol is open. The work is real. The web was built for eyes.

The next one will be built for minds.

Let's get to work.
