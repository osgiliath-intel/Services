# Example runs

Every business here is made up. The shapes are the ones we set up and run.

Legend: ⚙️ automation · 📏 fixed rules · 🤖 agent (model class shown) · 🧑 a person

## A campaign

A made-up café plans next month's posts.

```mermaid
flowchart LR
  A[⚙️ Gather dates, offers, past results<br><i>n8n</i>] --> B[🤖 Draft copy and images per channel<br><i>strong model via OpenRouter · Higgsfield</i>]
  B --> C[📏 Check consent, opt-outs, brand rules]
  C --> D{🧑 Owner approves}
  D --> E[⚙️ Schedule and record results<br><i>n8n</i>]
```

**The trace keeps:** which model wrote each draft and what it cost, which rules ran, who said yes and what they edited.

## Engineering

A made-up firm wants a change to its own system.

```mermaid
flowchart LR
  A[GitHub issue] --> B[🤖 Lead agent picks a ready issue]
  B --> C[🤖 Builder agent writes the change,<br>opens a pull request<br><i>Claude Code</i>]
  C --> D[⚙️ Tests and build<br><i>GitHub Actions</i>]
  D --> E[🤖 Independent review<br><i>a separate agent</i>]
  E --> F{🧑 A person approves anything<br>that changes the live system}
```

**The trace keeps:** the issue, every commit, the checks, the review verdict and the approval.

## Something happens

A scheduled health report comes in from a live system.

```mermaid
flowchart LR
  A[⚙️ Collect the health report] --> B[📏 Compare with what is expected]
  B --> C[🤖 Watcher agent gives a verdict<br><i>small model</i>]
  C --> D[⚙️ Alert a person's phone<br><i>ntfy</i>]
  D --> E{🧑 A person decides the fix}
```

**The trace keeps:** the report, the verdict and its reasons, when the alert went, what was decided.

## Research with several models

One question, each step on the model that suits it, all through one router key with a spending cap.

```mermaid
flowchart LR
  Q[A research question] --> A[🤖 Find our past notes<br><i>open-weight embedding model</i>]
  A --> B[🤖 Search the web, return sources<br><i>search model</i>]
  B --> W[🤖 Draft the brief<br><i>stronger model</i>]
  W --> C[🤖 Critique the draft<br><i>model from another lab</i>]
  C --> D[📏 Cheap check: sources present, question answered]
  D --> E{🧑 A person reads the brief}
  subgraph OpenRouter
    A
    B
    W
    C
  end
```

**The trace keeps:** model, tokens and cost per call, the sources returned, the flags the critic raised (Langfuse).

Open-weight models, such as the embedding model in the first step, are the kind published on Hugging Face. We reach ours through the router; we do not host or train models.
