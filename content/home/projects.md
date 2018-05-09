+++
# Projects widget.
widget = "projects"
active = true
date = 2016-04-20T00:00:00

title = "Projects"
subtitle = ""

# Order that this section will appear in.
weight = 50

# Content.
# Display content from the following folder.
# For example, `folder = "project"` displays content from `content/project/`.
folder = "project"

# View.
# Customize how projects are displayed.
# Legend: 0 = list, 1 = cards.
view = 1

# Filter toolbar.

# Default filter index (e.g. 0 corresponds to the first `[[filter]]` instance below).
filter_default = 0

# Add or remove as many filters (`[[filter]]` instances) as you like.
# Use "*" tag to show all projects or an existing tag prefixed with "." to filter by specific tag.
# To remove toolbar, delete/comment all instances of `[[filter]]` below.
[[filter]]
  name = "All"
  tag = "*"

[[filter]]
  name = "Statistical Genetics"
  tag = ".statgen"

[[filter]]
  name = "Network Analysis"
  tag = ".sna"

[[filter]]
  name = "Palaeoclimate Reconstruction"
  tag = ".bpr"

[[filter]]
  name = "Text Analysis"
  tag = ".text"

[[filter]]
  name = "Miscellaneous"
  tag = ".other"

+++

