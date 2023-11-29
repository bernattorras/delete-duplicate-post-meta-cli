# Delete Duplicate Post Meta Fields - WP-CLI-Command
A custom WP-CLI command to delete/export duplicate post meta fields.

# Options
- `[--dry-run]` - If set, no duplicate meta fields will be deleted.
- `[--post_id=<post_id>]` - If set, only the duplicate meta fields for the given post will be checked.
- `[--export=<export>]` - If set, the duplicate meta fields will be exported to a CSV file. Options:
    - `[none]` or `true` (default): Exports the count of duplicate meta fields.
    - `values`: Exports the duplicate meta values with their values.
 
# Examples
- `wp post delete-duplicate-meta --dry-run`

Checks how many duplicate post meta keys exist in the database.
  
- `wp post delete-duplicate-meta --export=values --dry-run`

Exports a list of the duplicate post meta keys with their values.

- `wp post delete-duplicate-meta --post_id=123 --export`

Deletes the duplicate meta keys of the post 123 and exports a list of the duplicate keys with a count of duplicate values.

- `wp post delete-duplicate-meta --export=values`

Deletes the duplicate meta keys of all the posts and exports:
- A list of the duplicate keys with a count of duplicate values
- A list of duplicated keys with their values.
