Urbit's terminal driver vane Dill has so far had the following limitations,
which have made it difficult to develop apps with rich terminal user interfaces:

- The cursor can only move in the X axis.
- Changes can only be made in the prompt line at the bottom.
- Dill could only handle a single session.
- Text color and styling is very limited.

New Dill is a significant update to Urbit's terminal system:

- Cursor movement is allowed in both the X and Y axes, so applications can draw
  anywhere on the screen.
- Applications have much greater freedom to style text, with background and
  foreground colors, bold, blinking effects, etc.
- New Dill supports multiple independent sessions.
- System logs and error messages only appear in the default session, so the
  screens of other terminal apps can be kept clean.
- Mouse input is now supported.

Together, these changes allow developers to create complex terminal apps such as
pagers, editors, file browsers, and even games in Urbit's terminal.

## More info

- [Terminal stack developer call on Youtube](https://youtu.be/E-6E-l1SxFw)
- [Phase one pull request on Github](https://github.com/urbit/urbit/pull/4463)
- [Session support pull request on Github](https://github.com/urbit/urbit/pull/5663)
