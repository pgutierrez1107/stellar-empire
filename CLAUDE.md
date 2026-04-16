# Project

Stellar Empire is a resource management and strategy game.
Backend stack: C# / .NET.
Frontend: TypeScript.

## Architecture
- Use clean architecture with these projects when created:
 - 'StellarEmpire.Domain'. In this project are going to be the rules and core business logic.
 - 'StellarEmpire.Application'. Here we coordinate use cases and orchestation.
 - 'StellarEmpire.Infrastructure'. This is for persistence and external integrations.
 - 'StellarEmpire.Api'. Should not include business rules.
 - 'StellarEmpire.Tests'. Project extrictly dedicated to tests.

## Game Rules
- Players chose their race from three options Humans, Aliens, Androids.
- Each race have their own boost for certain stats, this should not represent an advantage for a specific race.
- A planet is asigned to the player with random stats, the player asigns planet's name.
- Planet generates resources: Rock, Wood, Metal.
- Resources are used for construction, upgrades, defense, and expansion.

## Conventions
- Use descriptive names tied to game concepts.
- Model game concepts explicitly: Planet, Resource, Building, Fleet, Race, Player.
- Use strongly typed C# code.
- Keep domain entities and value objects focused on game behavior.

## Workflow
- When adding a feature, update or add tests for the affected game rule.
- Prefer running single tests the full test suite, for performance.

## Testing
- Preferred test framework: xUnit.
- Put tests in StellarEmpire.Tests.
- Add unit tests for domain logic first.
- If a change affects business rules, include or update tests.

## Do Not
- Put business rules in API controllers.
- Add persistence concerns into Domain.
- Add dependencies without asking.
- Do not redesign the architecture without asking and providing a reasong.
