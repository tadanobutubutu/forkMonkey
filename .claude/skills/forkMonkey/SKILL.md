```markdown
# forkMonkey Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill covers the development patterns and workflows used in the **forkMonkey** TypeScript project. The repository manages the evolution and state of a virtual monkey, with data and SVG image files tracking its progress. You'll learn about file organization, code style, and the main workflows for updating or initializing the monkey's state.

## Coding Conventions

### File Naming
- **Style:** kebab-case for files  
  **Example:**  
  ```
  monkey-evolution.ts
  monkey_data/history.json
  ```

### Imports
- **Style:** Relative imports  
  **Example:**
  ```typescript
  import { updateStats } from './monkey-utils';
  ```

### Exports
- **Style:** Named exports  
  **Example:**
  ```typescript
  export function evolveMonkey() { ... }
  export const MONKEY_VERSION = '1.0.0';
  ```

## Workflows

### Daily Monkey Evolution Update
**Trigger:** When someone wants to record the monkey's daily evolution.  
**Command:** `/evolve-monkey`

1. Update `README.md` with the latest evolution info or stats.
2. Update `monkey_data/history.json` with new historical data.
3. Update `monkey_data/stats.json` with new statistics.
4. Optionally update `monkey_data/dna.json` and `monkey_data/monkey.svg` if there are genetic or visual changes.
5. Generate a new SVG in `monkey_evolution/` with the current date and time.

**Example:**
```typescript
import { updateHistory, updateStats, generateSVG } from './monkey-utils';

updateHistory(newDayData);
updateStats(newStats);
generateSVG('monkey_evolution/2024-06-01_12-00_monkey.svg');
```

**Files Involved:**
- `README.md`
- `monkey_data/history.json`
- `monkey_data/stats.json`
- `monkey_data/dna.json` (optional)
- `monkey_data/monkey.svg` (optional)
- `monkey_evolution/YYYY-MM-DD_HH-MM_monkey.svg`

---

### Monkey Initialization
**Trigger:** When someone wants to create or reset the monkey's state.  
**Command:** `/init-monkey`

1. Create or reset `README.md` with initial information.
2. Create `monkey_data/dna.json` with starting DNA.
3. Create `monkey_data/history.json` with initial history.
4. Create `monkey_data/monkey.svg` with the initial monkey image.
5. Create `monkey_data/stats.json` with initial stats.
6. Generate an initial SVG in `monkey_evolution/` with the current date and time.

**Example:**
```typescript
import { initDNA, initHistory, initStats, generateSVG } from './monkey-utils';

initDNA();
initHistory();
initStats();
generateSVG('monkey_evolution/2024-06-01_00-00_monkey.svg');
```

**Files Involved:**
- `README.md`
- `monkey_data/dna.json`
- `monkey_data/history.json`
- `monkey_data/monkey.svg`
- `monkey_data/stats.json`
- `monkey_evolution/YYYY-MM-DD_HH-MM_monkey.svg`

## Testing Patterns

- **Framework:** Unknown (no specific testing framework detected)
- **File Pattern:** Test files are named with `*.test.*`  
  **Example:**  
  ```
  monkey-utils.test.ts
  ```
- **Style:** Tests are likely colocated with source files, using the `.test.` infix.

## Commands

| Command         | Purpose                                         |
|-----------------|-------------------------------------------------|
| /evolve-monkey  | Record the monkey's daily evolution             |
| /init-monkey    | Initialize or reset the monkey's state          |
```
