# Delta Spec: Analytics Dashboard View

## ADDED Requirements

### Requirement: Top Navigation Bar & Theme Switcher
The application header MUST use DaisyUI `navbar bg-base-100 border-b border-base-300` and include a brand title, dynamic theme selector dropdown, and notification badge.

#### Scenario: User switches visual theme
- Given the user selects `cyberpunk` from the theme dropdown selector,
- Then the root `<html>` element `data-theme` attribute changes to `cyberpunk`, updating all DaisyUI component colors instantly.

### Requirement: Responsive Metrics Stats Grid
The dashboard grid MUST contain a 3-column DaisyUI `stats` section (`grid grid-cols-1 md:grid-cols-3 gap-4`) for Total Revenue, Active Users, and Task Completion metrics.

#### Scenario: Viewing metrics on mobile device
- Given a user views the dashboard on a mobile screen (< 640px),
- Then the `stats` grid stacks vertically into a single column.

### Requirement: Data Table & Interactive Modal
The main content area MUST include a card container (`card bg-base-100 shadow-xl`) holding a DaisyUI zebra table (`table table-zebra`) and an action button that opens a DaisyUI modal `<dialog id="new_campaign_modal">`.

#### Scenario: User opens new campaign modal
- Given the user clicks the "New Campaign" primary button,
- Then the `<dialog id="new_campaign_modal">` opens with `.showModal()`.
