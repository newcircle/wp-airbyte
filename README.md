# wp-airbyte

This connector will take a Wordpress REST API end point for posts, parse out the following:

- id
- link
- title

For each nested entry under "block_data", extract the following and create a new row
- blockName
- attrs

For "innerBlocks", loop through recursively.

Do not create new row if blockName is one of the following:
- core/paragraph
- core/group
- core/image
- core/separator
- core/columns
- core/column
