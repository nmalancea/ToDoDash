# ToDo Dash

## Screens

### Homepage
- show all the tiers (1 tier per row)
- have a dropdown with number of tiers to show (default to “all")
- each list within a tier can not scroll vertically, but is clickable
- have a link to view all suggestions ahead

## Models

### Task
- description (string)
- isDone (boolean)
- previous (Task guid)
- next (Task guid)
- taskListId (belongsTo)

### TaskList
- name (string)
- tier (belongsTo)
- tasks (hasMany)

### Tier
- count per batch (default 1)
- previousTier (belongsTo)
- nextTier (belongsTo)
- showSuggestions (boolean, default false)

### Setting
- name (string)
- value (string)
- userId (belongsTo)

## Migrations
- set the showSuggestios for first 3 tiers to true


## Logic
### Suggestions

- highlight tier and todo square which needs to be done next
- show suggestions from the top 3 tiers only, by default
- tier 1 default count per batch is 3
- tier 2 default count per batch is 2
- tier 3 default count per batch is 1
- find total count per batch and calculate percentages, then pick tiers and tasks at random

## Settings
- number of tiers user picked on the homepage
