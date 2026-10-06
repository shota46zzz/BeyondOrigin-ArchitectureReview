# BeyondOrigin Architecture Review

This public repository stores visual evidence for reviewing Beyond Origin architecture. It is organized for all dungeons and structures, not just Central Temple.

## Directory convention

`architectures/<dungeon_id>/<architecture_id>/current/`

Example: `architectures/ancient_ruins/central_temple/current/`

Each architecture's `current/` directory contains `metadata.json` and review screenshots. `current/` holds the latest evidence. Identify the exact evidence used for a review by its Git commit hash; do not create iteration directories for routine versioning.

These files are review evidence. They are not runtime architecture assets or the source of truth for Structure NBT. Approved architecture is defined by Structure NBT in the main BeyondOrigin repository. An AI visual review PASS does not approve an architecture; final approval requires Human Review.
