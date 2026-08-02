# Graph Report - .  (2026-08-01)

## Corpus Check
- cluster-only mode — file stats not available

## Summary
- 299 nodes · 344 edges · 32 communities (28 shown, 4 thin omitted)
- Extraction: 99% EXTRACTED · 1% INFERRED · 0% AMBIGUOUS · INFERRED: 3 edges (avg confidence: 0.8)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `59721059`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- Community 0
- Community 1
- Community 2
- Community 3
- Community 4
- Community 5
- Community 6
- Community 7
- Community 8
- Community 9
- Community 10
- Community 11
- Community 12
- Community 13
- Community 14
- Community 15
- Community 16
- Community 17
- Community 18
- Community 19
- Community 20
- Community 21
- Community 22
- Community 23
- Community 24
- Community 25

## God Nodes (most connected - your core abstractions)
1. `compilerOptions` - 19 edges
2. `compilerOptions` - 16 edges
3. `compilerOptions` - 15 edges
4. `scripts` - 14 edges
5. `scripts` - 9 edges
6. `AppError` - 7 edges
7. `verifyInvitationCode()` - 5 edges
8. `RestaurantRepository` - 5 edges
9. `RestaurantUserRepository` - 5 edges
10. `exclude` - 5 edges

## Surprising Connections (you probably didn't know these)
- `buildTestApp()` --indirect_call--> `authenticate()`  [INFERRED]
  project/Restaurant3D/backend/src/middlewares/authenticate.test.ts → project/Restaurant3D/backend/src/middlewares/authenticate.ts
- `authenticate()` --calls--> `verifyAccessToken()`  [EXTRACTED]
  project/Restaurant3D/backend/src/middlewares/authenticate.ts → project/Restaurant3D/backend/src/shared/security/tokens.ts
- `exclude` --extends--> `generated`  [EXTRACTED]
  project/Restaurant3D/backend/tsconfig.build.json → project/Restaurant3D/backend/tsconfig.json
- `exclude` --extends--> `node_modules`  [EXTRACTED]
  project/Restaurant3D/backend/tsconfig.build.json → project/Restaurant3D/backend/tsconfig.json

## Import Cycles
- None detected.

## Communities (32 total, 4 thin omitted)

### Community 0 - "Community 0"
Cohesion: 0.10
Nodes (19): Db, RestaurantRepository, onboardRestaurant(), restaurantsService, OnboardingRequestDto, onboardingRequestSchema, OnboardingResponseDto, RestaurantsService (+11 more)

### Community 1 - "Community 1"
Cohesion: 0.08
Nodes (24): compilerOptions, allowArbitraryExtensions, allowImportingTsExtensions, erasableSyntaxOnly, jsx, lib, module, moduleDetection (+16 more)

### Community 2 - "Community 2"
Cohesion: 0.09
Nodes (22): author, description, keywords, license, main, name, scripts, build (+14 more)

### Community 3 - "Community 3"
Cohesion: 0.09
Nodes (22): dependencies, react, react-dom, react-router-dom, @tanstack/react-query, name, private, scripts (+14 more)

### Community 4 - "Community 4"
Cohesion: 0.10
Nodes (21): bcryptjs, cors, dotenv, express, helmet, jsonwebtoken, morgan, @prisma/adapter-mariadb (+13 more)

### Community 5 - "Community 5"
Cohesion: 0.10
Nodes (20): devDependencies, eslint, prettier, supertest, tsx, @types/bcryptjs, @types/express, @types/jsonwebtoken (+12 more)

### Community 6 - "Community 6"
Cohesion: 0.10
Nodes (19): compilerOptions, allowImportingTsExtensions, erasableSyntaxOnly, lib, module, moduleDetection, noEmit, noFallthroughCasesInSwitch (+11 more)

### Community 7 - "Community 7"
Cohesion: 0.11
Nodes (19): eslint-plugin-react-hooks, eslint-plugin-react-refresh, devDependencies, eslint-plugin-react-hooks, eslint-plugin-react-refresh, prettier, tailwindcss, @tailwindcss/vite (+11 more)

### Community 8 - "Community 8"
Cohesion: 0.20
Nodes (8): authenticate(), buildTestApp(), errorHandler(), validateRequest(), restaurantsRouter, app, AppError, ErrorDetail

### Community 9 - "Community 9"
Cohesion: 0.12
Nodes (17): compilerOptions, esModuleInterop, forceConsistentCasingInFileNames, lib, module, moduleResolution, noFallthroughCasesInSwitch, noUnusedLocals (+9 more)

### Community 10 - "Community 10"
Cohesion: 0.17
Nodes (11): exclude, extends, dist, exclude, include, dist, generated, node_modules (+3 more)

### Community 11 - "Community 11"
Cohesion: 0.36
Nodes (7): generateInvitationCode(), getSecret(), InvitationPayload, InvitationVerificationResult, sign(), verifyInvitationCode(), code

### Community 12 - "Community 12"
Cohesion: 0.43
Nodes (3): App(), router, queryClient

### Community 13 - "Community 13"
Cohesion: 0.33
Nodes (5): printWidth, semi, singleQuote, tabWidth, trailingComma

### Community 14 - "Community 14"
Cohesion: 0.33
Nodes (5): printWidth, semi, singleQuote, tabWidth, trailingComma

### Community 15 - "Community 15"
Cohesion: 0.50
Nodes (3): AuthContext, Express, Request

### Community 16 - "Community 16"
Cohesion: 0.67
Nodes (3): eslint-config-prettier, eslint-config-prettier, eslint-config-prettier

### Community 17 - "Community 17"
Cohesion: 0.67
Nodes (3): @eslint/js, @eslint/js, @eslint/js

### Community 18 - "Community 18"
Cohesion: 0.67
Nodes (3): globals, globals, globals

### Community 19 - "Community 19"
Cohesion: 0.67
Nodes (3): @types/node, @types/node, @types/node

### Community 20 - "Community 20"
Cohesion: 0.67
Nodes (3): typescript, typescript, typescript

### Community 21 - "Community 21"
Cohesion: 0.67
Nodes (3): typescript-eslint, typescript-eslint, typescript-eslint

## Knowledge Gaps
- **149 isolated node(s):** `semi`, `singleQuote`, `trailingComma`, `printWidth`, `tabWidth` (+144 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **4 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `devDependencies` connect `Community 5` to `Community 2`, `Community 16`, `Community 17`, `Community 18`, `Community 19`, `Community 20`, `Community 21`, `Community 23`, `Community 24`, `Community 25`?**
  _High betweenness centrality (0.123) - this node is a cross-community bridge._
- **Why does `devDependencies` connect `Community 7` to `Community 3`, `Community 5`, `Community 16`, `Community 17`, `Community 18`, `Community 19`, `Community 20`, `Community 21`?**
  _High betweenness centrality (0.096) - this node is a cross-community bridge._
- **Why does `dependencies` connect `Community 4` to `Community 2`?**
  _High betweenness centrality (0.053) - this node is a cross-community bridge._
- **What connects `semi`, `singleQuote`, `trailingComma` to the rest of the system?**
  _149 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Community 0` be split into smaller, more focused modules?**
  _Cohesion score 0.09523809523809523 - nodes in this community are weakly interconnected._
- **Should `Community 1` be split into smaller, more focused modules?**
  _Cohesion score 0.08 - nodes in this community are weakly interconnected._
- **Should `Community 2` be split into smaller, more focused modules?**
  _Cohesion score 0.08695652173913043 - nodes in this community are weakly interconnected._