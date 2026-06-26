# Issue 19 Rendering Comparison

These screenshots use the same mocked Inspect log at a 1280-pixel viewport.
The log contains:

- one typed `ContentReasoning` block;
- visible text before and after the tag-like content; and
- literal `<think>`, `<internal>`, and `<content-internal>` blocks.

## Before

Captured from unmodified `ts-mono` upstream `main` at `8241571`.

![Before remediation](before.png)

The typed reasoning block renders normally, but all three literal blocks and
their enclosed text are deleted from the displayed evidence.

## After

Captured from `fix/render-literal-reasoning-tags`.

![After remediation](after.png)

Typed reasoning retains its dedicated presentation. Literal tag-like text is
escaped and displayed as evidence.
