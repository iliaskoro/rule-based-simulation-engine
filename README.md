# Rule-Based Simulation Engine – OOP Architecture & Deterministic State

A modular C++ object-oriented simulation engine inspired by MasterChef-style competitive shows.  
It models players, teams, multiple competition types, awards, and voting mechanics using clean OOP design and extensible architecture.

## Features

### Core Entities

- Player class
- Team class with scoring and state logic.
- Competition base class with extensible design.
- Award hierarchy enabling multiple award types.

### Competition Types

- Immunity Competition
- Creativity Competition
- Team Competition
- (Easily extendable with new competition types)

### Awards

- Immunity Award  
- Food Award  
- Excursion Award  

### Voting System

Standalone Voting module implementing rating & decision models.

---

## Project Structure

```
/
├── src/
│   ├── core/
│   │   ├── Player.cpp/h
│   │   ├── Team.cpp/h
│   │   ├── Competition.h
│   │   ├── Award.h
│   │   ├── Round.h
│   │   └── main.cpp
│   │
│   ├── competitions/
│   │   ├── ImmunityCompetition.cpp/h
│   │   ├── CreativityCompetition.cpp/h
│   │   └── TeamCompetition.cpp/h
│   │
│   │
│   ├── awards/
│   │   ├── ImmunityAward.h
│   │   ├── FoodAward.h
│   │   └── ExcursionAward.h
│   │
│   └── voting/
│       ├── Voting.cpp/h
│       └── Vote.h
│
├── docs/
│   ├── diagrams/
│   └── architecture.md
│
├── CMakeLists.txt
├── .gitignore
└── README.md
```

---

## Build Instructions (CMake)

```
mkdir build
cd build
cmake ..
cmake --build .
./masterchef
```

## UML & Architecture

See `docs/architecture.md` and `docs/diagrams/`.

## Extending the Engine

### To add a new Competition:
1. Derive from `Competition`
2. Override scoring logic
3. Integrate award callbacks

### To add a new Award:

1. Derive from `Award`
2. Implement `apply(Player&)`

## Author
Ilias Korompilis

## License
MIT License.


