# turbo

## Methodology

- https://github.com/cumbucadev/mentoria/tree/main/mentoria/metodologia

## Theory

Git and Github
- https://git-e-github.para-humanos.cumbuca.dev/ (book)
- https://linuxtips.io/treinamentos-essentials/ (course pt-br)

Python (60 horas)
- https://runestone.academy/ns/books/published/thinkcspy/index.html
- https://linuxtips.io/treinamento/python-base/ (course pt-br)

Tests

## Practice (Guided Work): Project

## Practice (Independent Work): Project Drink Recipes

### Project goal

Build a Python command-line application to manage drink recipes, while learning:

* Terminal usage
* Git & GitHub workflows (local branches, remote branches, PRs)
* Python fundamentals
* Basic testing
* Realistic data modeling and refactoring

---

## Phase 0 — Environment Setup & Git Basics

### Theory

* Terminal basics (`cd`, `ls`, `mkdir`)
* What Git is and why it exists
* Local vs remote repositories

### Tasks

* Create `drink-recipes/`
* Initialize Git
* Create `README.md`
* First commit on `main`

---

## Phase 1 — First Python Script (Input & Output)

### Theory

* `print`, `input`
* Variables
* Running Python from terminal

### Tasks

* Create `main.py`
* Print a welcome message
* Ask user’s name and greet them
* Commit to `main`

---

## Phase 2 — Initial Data Model (Lists & Dictionaries)

### Theory

* Lists
* Dictionaries
* Simple data modeling

### Tasks

* Model a drink:

  ```python
  {
    "name": "Mojito",
    "ingredients": ["rum", "mint", "lime", "sugar", "soda"],
    "steps": "Mix and serve"
  }
  ```
* Store drinks in a list
* Print drink names
* Commit

---

## Phase 3 — Control Flow & Menu

### Theory

* `if / elif / else`
* `for` and `while` loops

### Tasks

* Create menu:

  ```
  1 - List drinks
  2 - View drink
  3 - Exit
  ```
* Handle user input
* Commit

---

## Phase 4 — Functions & Local Branches

### Theory

* Functions
* Code organization
* Why branches exist

### Tasks

* Create local branch:

  ```bash
  git checkout -b refactor-functions
  ```
* Extract functions:

  * `menu()`
  * `list_drinks()`
  * `show_drink(name)`
* Merge into `main`
* Delete branch

---

## Phase 5 — Adding Recipes (Ingredients with `;`)

### Theory

* String manipulation
* `.split()`
* Mutating lists

### Tasks

* Create branch:

  ```bash
  git checkout -b add-drink
  ```
* Add menu option:

  ```
  4 - Add new drink
  ```
* Ask ingredients using **`;` as separator**:

  ```
  rum; mint; lime; sugar; soda
  ```
* Convert to list with `split(";")`
* Keep `steps` as a **single string**
* Merge into `main`

---

## Phase 6 — Persistence with Files

### Theory

* File I/O
* JSON (`json.load`, `json.dump`)

### Tasks

* Create branch:

  ```bash
  git checkout -b persist-recipes
  ```
* Save drinks to `drinks.json`
* Load on startup
* Merge into `main`

---

## Phase 7 — Basic Testing

### Theory

* Why tests exist
* Unit tests
* `unittest` or `pytest`

### Tasks

* Create branch:

  ```bash
  git checkout -b add-tests
  ```
* Create `tests/`
* Tests for:

  * Ingredient parsing using `;`
  * Adding a drink
* Run tests locally
* Merge into `main`

---

## Phase 8 — Refactor: `steps` as a List (Key Learning Phase)

### Theory

* Lists revisited
* Refactoring safely
* Updating data models
* Regression tests

### Tasks

* Create branch:

  ```bash
  git checkout -b steps-as-list
  ```
* Change `steps` from:

  ```python
  "steps": "Mix and serve"
  ```

  to:

  ```python
  "steps": [
    "Add ingredients to the glass",
    "Mix gently",
    "Serve with ice"
  ]
  ```
* Ask user to input steps separated by `;`
* Display steps as a numbered list
* Update existing recipes if needed
* Update tests
* Push branch and open a **Pull Request**
* Review and merge via GitHub

---

## Phase 9 — GitHub Workflow (Remote Branches & PRs)

### Theory

* Remote branches
* Pull Requests
* Code review basics

### Tasks

* Push repo to GitHub (if not already)
* Create remote branch:

  ```bash
  git checkout -b search-by-ingredient
  git push -u origin search-by-ingredient
  ```
* Open PR
* Use PR discussion for feedback
* Merge via GitHub UI

---

## Phase 10 — Search & Filter (via PR)

### Theory

* String comparison
* Case-insensitive matching
* Looping through nested lists

### Tasks

* Implement:

  ```
  5 - Search drinks by ingredient
  ```
* Match against ingredient list
* Add/update tests
* Merge via PR

---

## Phase 11 — Error Handling & Edge Cases

### Theory

* `try / except`
* Input validation

### Tasks

* Handle:

  * Invalid menu options
  * Empty ingredient or step lists
* Fix via branch + PR

---

## Phase 12 — Polish & Documentation

### Theory

* Clean code
* Documentation basics

### Tasks

* Improve `README.md`:

  * Project overview
  * How to run
  * How to run tests
* Final review of commit history and PRs

---

## Final Outcome

By the end, the mentee will have:

* A **real Python CLI application**
* Hands-on experience with:

  * Git branches (local & remote)
  * Pull Requests
  * Refactoring safely
  * Basic automated testing
* A strong foundation for real-world software development

If you want, I can next:

* Turn this into a **week-by-week mentoring plan**
* Provide **example test cases**
* Create a **mentor checklist per phase**




