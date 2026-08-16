# Open and Review in VS Code

The purpose of this step is to prove that the repository is not only a collection of screenshots. The source files must open, be understandable and match the visual exports.

## 1. Open the repository

1. Extract the ZIP.
2. Open VS Code.
3. Choose **File → Open Folder**.
4. Select `Module-01-Documentation-and-system-design-FULL`.

## 2. Review the documentation

Open:

`docs/System-Design-Documentation.md`

Use the Markdown preview if you want a formatted view.

## 3. Review each diagram

For each diagram:

1. Open the `.mmd` source.
2. Open the matching `.svg` preview.
3. Split the editor so source and visual can be seen together.
4. Read the design question in the matching `.md` file.
5. Confirm that you can explain every actor, process, flow, entity, relationship and screen.

Example:

```text
diagrams/04-erd/
├── erd.mmd
├── erd.md
└── erd.svg
```

## 4. Take your screenshots

Follow:

`evidence/screenshots/README.md`

The screenshots should come from **your own VS Code environment**. Do not edit personal data into the repository.

## 5. Send the screenshots back for review

The review will check:

- source readability
- diagram logic
- consistency between diagrams
- traceability to requirements
- whether the visual output matches the source
- naming and repository cleanliness
- what should be fine-tuned before GitHub publication

## 6. Your final check

You should be able to explain:

> Why does every item in this system exist?

If the answer is only “because the diagram needed it,” the design needs more work.
