# Product Requirements Document (PRD) - TODO App Upgrade

## 1. Overview

We are upgrading the basic TODO app to make it more useful while keeping the implementation simple and teachable. The MVP will add due dates, task priorities, and quick filters so users can better organize and review their work. The solution should remain local-only, with no backend changes or external storage.

---

## 2. MVP Scope

- Add an optional `dueDate` field for each task.
- Store `dueDate` in ISO `YYYY-MM-DD` format.
- Add a `priority` field for each task with allowed values `P1`, `P2`, or `P3`.
- Default `priority` to `P3` when a new task is created.
- Add filters for `All`, `Today`, and `Overdue`.
- Keep storage local only.
- Do not introduce backend changes.
- Validate task data as follows:
  - `title` is required.
  - `priority` must be `P1`, `P2`, or `P3`.
  - `dueDate` is optional.
  - Invalid `dueDate` values should be ignored and treated as absent.

---

## 3. Post-MVP Scope

- Visually highlight overdue tasks so they stand out.
- Add sorting with the following order:
  - overdue tasks first
  - then by priority from `P1` to `P3`
  - then by due date in ascending order
  - tasks without a due date last

---

## 4. Out of Scope

- Notifications
- Recurring tasks
- Multi-user support
- Keyboard navigation enhancements
- External storage
- Any backend work beyond the existing local-only application design
