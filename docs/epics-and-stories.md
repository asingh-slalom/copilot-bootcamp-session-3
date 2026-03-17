# Epics and Stories - TODO App Upgrade

Based on the requirements in `docs/prd-todo.md` and organized using the structure from `docs/templates/epic-and-stories-template.md`.

## Epics

### MVP

- Task Details
- Task Filtering
- Task Validation and Local-Only Behavior

### Post-MVP

- Overdue Task Visibility
- Task Sorting

## Stories

### MVP

#### Epic: Task Details

- Add due date field to tasks
- Store due dates in YYYY-MM-DD format
- Add priority field to tasks
- Default new tasks to P3 priority

#### Epic: Task Filtering

- Add All tasks filter
- Add Today tasks filter
- Add Overdue tasks filter

#### Epic: Task Validation and Local-Only Behavior

- Require a title for each task
- Restrict priority values to P1, P2, or P3
- Treat due date as optional
- Ignore invalid due date values
- Keep task data local only
- Preserve the existing frontend-only design

### Post-MVP

#### Epic: Overdue Task Visibility

- Highlight overdue tasks in the task list

#### Epic: Task Sorting

- Sort overdue tasks before other tasks
- Sort tasks by priority from P1 to P3
- Sort tasks with due dates in ascending order
- Place tasks without due dates last

## Acceptance Criteria

### MVP

- Tasks may include an optional due date.
- Due dates are stored in ISO `YYYY-MM-DD` format.
- Tasks include a priority value limited to `P1`, `P2`, or `P3`.
- New tasks default to priority `P3`.
- Users can filter tasks by `All`, `Today`, and `Overdue`.
- Task titles are required.
- Invalid due date values are ignored and treated as absent.
- The solution remains local-only.
- No backend changes are introduced.

### Post-MVP

- Overdue tasks are visually highlighted.
- Tasks are sorted with overdue tasks first.
- Remaining tasks are sorted by priority from `P1` to `P3`.
- Tasks with due dates are sorted in ascending date order.
- Tasks without due dates appear last.

## Technical Requirements

- Keep the implementation local-only with no external storage.
- Do not introduce backend changes beyond the existing frontend-only application design.
- Store `dueDate` values in ISO `YYYY-MM-DD` format.
- Validate `title` as required input.
- Validate `priority` against the allowed values `P1`, `P2`, and `P3`.
- Treat `dueDate` as optional.
- Ignore invalid `dueDate` values and treat them as absent.
- Implement filters for `All`, `Today`, and `Overdue`.
- Implement overdue highlighting as a Post-MVP enhancement.
- Implement sorting in this order: overdue first, then priority `P1` to `P3`, then due date ascending, then tasks without due dates last.