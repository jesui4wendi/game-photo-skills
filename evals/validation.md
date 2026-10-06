# Packaging and browser checks

- Skill Creator format validator passes for the source folder and the extracted standalone archive.
- UI metadata is valid YAML; the short description and explicit skill invocation meet the documented constraints.
- Markdown references resolve in the repository and inside the extracted Skill; all three recipe / review documents are contained in the archive.
- Browser review verified both preset switches, both scene switches, loaded images, keyboard movement of the divider, and its 0 / 100 endpoints. The observed narrow layout had no horizontal overflow.
- No paid API, model SDK, account credential or engine asset is packaged. Generation uses the host image editor.
- Seven actual input-image edits and their creating-assistant visual review are recorded separately in `README.md`, `prompts.json` and `results.json`; these checks do not certify game fidelity.

The public preview images are resized JPEGs; the original generated PNG files are retained locally. The standalone Skill does not need the example images to operate.
