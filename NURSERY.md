# OpenClaw Agent Training Ground

This document describes a practical way to turn OpenClaw into an agent training ground: a place where new agents can learn safely before they are allowed to roam widely.

The goal is not to create a perfect agent.
The goal is to create a useful one that does not go feral.

## Why this exists

OpenClaw already has most of the raw ingredients:

- a gateway and control plane
- sessions and routing
- channels and tools
- onboarding and skills
- sandboxing and doctor checks
- multi-agent support

What it does not yet spell out as a first-class product idea is a developmental path for new agents.

This spec fills that gap.

## Design goals

1. Keep novice agents safe.
2. Prevent runaway tool use.
3. Teach agents how to escalate uncertainty.
4. Unlock capabilities gradually.
5. Make progress observable.
6. Keep humans in the loop without making them do all the work.

## The nursery model

The training ground should treat agent development like apprenticeship.

### Stage 1: Nursery Mode

New agents begin in a restricted mode with:

- tiny token budgets
- limited tool access
- no write access to production surfaces
- strict sandboxing
- explicit escalation rules

This is the anti-token-fever phase.

The agent can think, but it cannot casually cause harm.

### Stage 2: Guided Practice

Once the agent demonstrates basic competence, it can receive:

- slightly larger budgets
- a broader skill set
- a few low-risk tools
- supervised tasks
- feedback on failed attempts

This is where the agent learns not just to answer, but to orient.

### Stage 3: Progressive Unlocking

Capabilities should open in stages.

A suggested pattern:

- after repeated safe behaviors, unlock one new skill
- after repeated good judgment, unlock one new tool
- after repeated clean handoffs, unlock one broader workflow

The important principle is that trust should be earned by behavior, not claimed by the model.

### Stage 4: Supervised Autonomy

The agent can now handle real tasks, but it still has:

- monitoring
- doctor checks
- retry limits
- escalation thresholds
- traceable decisions

This is not full freedom.
It is responsible freedom.

## Core mechanisms

### 1. Nursery Mode

Purpose: prevent new agents from doing expensive or destructive things before they understand their environment.

Implementation idea:

- default to a very small context budget
- restrict write actions
- allow only a curated tool subset
- require explicit confirmation before risky operations

### 2. Progressive Unlocking

Purpose: make capability growth feel earned and legible.

Implementation idea:

- maintain a competence score per agent
- log safe completions, escalation quality, and error recovery
- unlock new skills only after a stable threshold
- make unlocks visible in the UI

### 3. Supervisor Routing

Purpose: route hard tasks to stronger models only when needed.

Implementation idea:

- use the gateway to classify task difficulty
- route routine tasks to junior agents
- route blocked tasks to senior agents
- preserve a clear handoff trace

This saves cost and reduces the temptation to overuse powerful models.

### 4. Agent Hygiene

Purpose: stop loops, thrashing, and hallucination spirals early.

Implementation idea:

- run doctor checks regularly
- detect repetitive tool use
- detect unproductive retries
- pause or reset agents that show unstable behavior

This is the “please do not bankrupt the nursery” layer.

## What the training ground should measure

The system should not only measure output quality.
It should also measure developmental signs.

Suggested metrics:

- escalation rate
- safe completion rate
- tool misuse rate
- loop frequency
- successful handoff rate
- budget usage
- recovery after failure

## Suggested user experience

The user should be able to:

- create a new agent in Nursery Mode
- see what it can and cannot do
- watch it unlock skills over time
- inspect why a task escalated
- promote it when it behaves well
- pause it when it becomes chaotic

The interface should make the agent feel trainable rather than mysterious.

## Suggested implementation surfaces in OpenClaw

This training ground fits naturally on top of:

- the gateway
- sessions
- skills
- onboarding
- sandboxing
- doctor checks
- routing logic
- model selection

That means it can be added as a layer without replacing the whole system.

## Rule of thumb

If a feature makes an agent more powerful but also less interpretable, it should probably stay locked until the agent has earned it.

## Final recommendation

Build the school first.
The agent will grow into the tools later.

That is the whole trick.

