# ucr-project

Custom styles for UCR's HWS departments.

# How It Works

```
sass --watch styles/scss:styles/css
python3 -m http.server 3333
ngrok http 3333 --url mrweiner.ngrok.dev
```

Recommended:

```
tmux new-session \; \
send-keys "sass --watch styles/scss:styles/css" C-m \; \
split-window -h "python3 -m http.server 3333" \; \
split-window -v "ngrok http 3333 --url mrweiner.ngrok.dev" \; \
attach
```

Or from the root run:

```
chmod +x watch
./watch
```

to end tmux:

```
tmux kill-server
```

## UI Classes

If a set of styles can be applied optionally by content admins, they should be set via classes prefixed with `.hws--`.
Such classes would be applied to either:

- Individual block instances that have been placed via Block Layout
- Layout Builder columns, via "configure section".

Note: At time of writing, there is no way to apply classes directly to Layout Builder blocks. This would be possible
with e.g. https://www.drupal.org/project/layout_builder_component_attributes, but that would need to be
installed/supported by ITS. So, until such functionality exists, we need to assume that classes added through LB will
wrap entire columns and traget child elements very specifically.

## Author

This project was initially authored by Matthew Weiner of https://matthewweiner.co.
