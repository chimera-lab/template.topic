# Flow Test

## Flow

    ┌─────────┐
    │  /init  │────── fail ─────┐
    └────┬────┘                 │
         │ ok                   │
         ↓                      │
    ┌─────────┐                 │
    │  /plan  │◄────────────┐   │
    └────┬────┘             │   │
         │ ok               │   │
         ↓                  │   │
    ┌──────────┐            │   │
    │ /execute │── fail ────┤   │
    └────┬─────┘            │   │
         │ ok               │   │
         ↓                  │   │
    ┌─────────┐             │   │
    │ /review │── fail ─────┘   │
    └────┬────┘                 │
         │ ok                   │
         ↓                      │
    ┌──────────┐                │
    │ /validate│── fail ────────┘
    └──────────┘
         │ ok
         ↓
      [done]

## Flow Requirements Table

| FLOW                | Agents                                      | Knowledge                             | Prompts                   | Docs                                                               |
| ------------------- | ------------------------------------------- | ------------------------------------- | ------------------------- | ------------------------------------------------------------------ |
| `/init`             | Organization Manager                        | Fundamentals, Repository              | Init                      | Organization, Architecture, Readme,                                |
| `/plan`             | Project Manager                             | Planning, Fundamentals, Repository    | Plan                      | Structure, Roadmap                                                 |
| `/execute`          | Developer                                   | Execution, Planning, Fundamentals     | Execute                   | Development, Architecture, Structure                               |
| `/review`           | Project Manager                             | Review, Execution, Planning           | Review                    | Security, Architecture, Development                                |
| `/validate`         | Repository Manager                          | Validation, Review                    | Validate, Commit          | Contributing, Changelog, Code of Conduct                           |

## Architecture Notes

**Agent → Knowledge → Docs Flow**:

- Agents consume Knowledge (machine-optimized information)
- Knowledge fundamentates Docs (human-readable documentation)
- Docs column shows which documentation is fundamentated by the knowledge bases used

**Multi-Agent Phases**:

- Multiple agents can collaborate per phase when responsibilities require different expertise
- Primary agent listed first, supporting agents follow

**Failure Paths**:

- `/init` fail → restart (fundamental setup issue)
- `/execute` fail → return to `/plan` (implementation revealed plan issues)
- `/review` fail → return to `/plan` (quality issues require replanning)
- `/validate` fail → return to `/init` (documentation/contribution standards violated)

**Knowledge Composition**:

- Phases consume multiple knowledge bases as needed
- Later phases inherit context from earlier knowledge (Planning includes Fundamentals, Execution includes Planning+Fundamentals)

**Phase Responsibilities**:

- `/init`: Understand context, setup environment, validate architecture fit
- `/plan`: Define approach, break down tasks, set success criteria
- `/execute`: Implement changes, run tests, verify functionality
- `/review`: Validate quality, security, architecture compliance, test coverage
- `/validate`: Ensure documentation complete, changelog updated, contribution standards met
