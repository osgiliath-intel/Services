# Example runs

Every business here is made up. The shapes are the ones we set up and run. Each step shows who does it (an automation, fixed rules, an agent or a person), the kind of model if it uses one, and the software it touches.

## A campaign

<p align="center"><picture>
  <source media="(prefers-color-scheme: dark)" srcset="../assets/run-campaign-dark.png">
  <img src="../assets/run-campaign-light.png" alt="Campaign run: gather dates, offers and past results (n8n); draft copy and images (stronger model, OpenRouter, Higgsfield); check consent, opt-outs and brand rules; the owner approves; schedule and record results." width="720">
</picture></p>

## Engineering

<p align="center"><picture>
  <source media="(prefers-color-scheme: dark)" srcset="../assets/run-engineering-dark.png">
  <img src="../assets/run-engineering-light.png" alt="Engineering run: a lead agent picks a ready issue; a builder agent opens a pull request; tests and build run; a separate agent reviews; a person approves anything that changes the live system." width="720">
</picture></p>

## Something happens

<p align="center"><picture>
  <source media="(prefers-color-scheme: dark)" srcset="../assets/run-event-dark.png">
  <img src="../assets/run-event-light.png" alt="Event run: collect the health report; compare with what is expected; a watcher agent gives a verdict on a small model; alert a phone with ntfy; a person decides the fix." width="720">
</picture></p>

## Research with several models

<p align="center"><picture>
  <source media="(prefers-color-scheme: dark)" srcset="../assets/run-research-dark.png">
  <img src="../assets/run-research-light.png" alt="Research run: find past notes (open-weight embedding model), search the web (search model), draft (stronger model), critique (model from another lab), flag what needs a person, then a person reads the brief." width="720">
</picture></p>

Open-weight models, such as the embedding model in the first step, are the kind published on Hugging Face. We reach ours through the router; we do not host or train models.

## One key, several models

<p align="center"><picture>
  <source media="(prefers-color-scheme: dark)" srcset="../assets/models-dark.png">
  <img src="../assets/models-light.png" alt="Each step of a job goes to the model that suits it, through one OpenRouter key with a spending cap. A person signs off, and Langfuse keeps one trace." width="720">
</picture></p>
