# P.A.S.S. (Pier Access Sequence System) (Showcase)

An early-stage logistics product that aims to cut the time drayage truckers spend picking up containers at the Ports of Los Angeles and Long Beach.

> This is a showcase repo. P.A.S.S. is in active development as a potential startup, so the source code, algorithms, results, and screenshots are private. A walkthrough is available on request.

**Contact:** jahan.atkins815@gmail.com | [linkedin.com/in/jahan-atkins-39002b419](https://linkedin.com/in/jahan-atkins-39002b419)

## The problem

Drayage truckers are paid by the load, not by the hour, so every minute spent waiting inside a marine terminal is unpaid time. Terminals lose too, because inefficient pickups waste expensive crane work. Both sides pay for the same inefficiency.

## The approach

P.A.S.S. is a sequencing optimizer: it decides the order in which trucks are served so that the terminal's equipment works more efficiently and drivers get in and out faster. The goal is a single change that saves time for the trucker and money for the terminal at once.

## What's built so far

- **Core engine:** a framework-free Python model of terminal operations plus a set of sequencing strategies, from a first-come-first-served baseline up to more advanced approaches
- **Simulator and benchmark harness:** a discrete-event simulator that tests each strategy across many randomized runs, including control scenarios where a real improvement should not appear
- **API:** a FastAPI service for the backend
- **Integrations layer:** adapters for connecting to outside terminal and port data sources
- **Mobile app:** an Expo (React Native) driver app, in progress

## Tech stack

| Layer | Tools |
|---|---|
| Core logic | Python, NumPy, SimPy |
| Backend | FastAPI |
| Mobile | Expo (React Native), TypeScript |
| Database | Postgres with PostGIS (planned) |
| Testing | pytest, Hypothesis (property-based testing), ruff, mypy |
| Infrastructure | Docker, CI |

## Engineering approach

- **Prove it before you sell it.** Every sequencing strategy has to beat the baseline in the simulator before it ships, and one advanced strategy was built, benchmarked, and dropped because it didn't pay off.
- **Honest milestones.** The project is planned in milestones with written acceptance criteria, and design decisions are recorded as architecture decision records (ADRs).
- **Clean separation.** The core engine has no web framework or database code, so it can be tested on its own and reused anywhere.

## My role

Co-founder working with Lamour Atkins and Quinton Jones. I built the MVP software: the core engine, simulator, and backend.

## What I learned

- Turning a real logistics problem into a measurable software design
- Using simulation and controls to tell a real improvement from noise
- Property-based testing for code where correctness really matters
- Recording decisions so a small team stays aligned
