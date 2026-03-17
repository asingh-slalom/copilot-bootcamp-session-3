# Epics and Stories - TODO App Upgrade

Based on the requirements in `docs/prd-todo.md` and organized using the structure from `docs/templates/epic-and-stories-template.md`.

## MVP Epics

- Epic: Task Details
  - Story: Add due date field to tasks
  - Story: Store due dates in YYYY-MM-DD format
  - Story: Add priority field to tasks
  - Story: Default new tasks to P3 priority

- Epic: Task Filtering
  - Story: Add All tasks filter
  - Story: Add Today tasks filter
  - Story: Add Overdue tasks filter

- Epic: Task Validation and Local-Only Behavior
  - Story: Require a title for each task
  - Story: Restrict priority values to P1, P2, or P3
  - Story: Treat due date as optional
  - Story: Ignore invalid due date values
  - Story: Keep task data local only
  - Story: Preserve the existing frontend-only design

## Post-MVP Epics

- Epic: Overdue Task Visibility
  - Story: Highlight overdue tasks in the task list

- Epic: Task Sorting
  - Story: Sort overdue tasks before other tasks
  - Story: Sort tasks by priority from P1 to P3
  - Story: Sort tasks with due dates in ascending order
  - Story: Place tasks without due dates last