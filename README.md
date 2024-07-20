# Draw.io Interactive Diagrams

This is a super small repo that includes two files:

- a draw.io file
- an HTML export of the diagram in that draw.io file

The purpose of this repo and the files within is to show how you can create and export interactive diragrams in draw.io. In this example, I show how a user would authenticate using OAuth 2.0 and an external IDP to retrieve a web-based resource through a public gateway.

When I diagram systems, I use this approach to show how data progresses through a system in a way that non-technical stakeholders can easily understand.

## Actions and Tags

The key to interactive diagrams is to add `tags` to each element that you want to show or hide, and then `action` links to the interactive elements that will trigger different elements to appear or disappear, based on the tags applied.

To view the `tags` on different elements in the `components` layer, use `Cmd+M` (or `Ctrl+M` on Windows) to open that element's `data` attributes pane.  It will show the list of `tags` that have been applied, in a space-delimited list.

To view the `actions` associated with each of the text blocks in the `text-links` layer, use `Option+Shift+L` (or `Alt+Shift+L` on Windows). That will show an associated link that takes the form of a text tuple, with the first element being a key-value pair declaring the type of link being used, and the second being a JSON block describing what actions should be taken, in array form.

Note that when you have multiple actions listed, they are applied in order. So let's say we have an action that will hide all elements with the tag `"steps"`, and show all elements with the tag `"1"`. If the actions are written in that order, then all elements except those with the tag `"1"` will be hidden, even if thos elements also have the `"steps"` tag.
