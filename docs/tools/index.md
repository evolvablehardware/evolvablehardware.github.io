# Tools

This should explain that this is general background information needed to understand what is happening. This should link out to the other sub-pages. Maybe using cards, see `mkdocs.yml`.

<div class="grid cards" markdown>

-   :fontawesome-solid-wrench:{ .lg .middle } __Tool Template__

    ---

    This is an example tool to demonstrate what a tool would actually look like to be filled in later.

    [:octicons-arrow-right-24: Learn More](./tool_template/index.md)<br>
    [:fontawesome-solid-graduation-cap: Tutorials](./tool_template/tutorials/index.md)<br>
    [:fontawesome-solid-sheet-plastic: Reference Sheet](./tool_template/reference_sheet.md)<br>
    [:material-file-document-multiple: Documentation](./tool_template/docs/index.md)

-   :material-thermometer-probe:{ .lg .middle } __Add Another Project__

    ---

    This is just to show that there is in fact a grid.

    [:octicons-arrow-right-24: Select an Icon](https://squidfunk.github.io/mkdocs-material/reference/icons-emojis/)

</div>

## Structure of Tools Folder

It would be good to separate out software tools like git from hardware platforms. Here, software is included in hardware platforms so long as it only applies to that particular platform, otherwise it is a software tool.

- Name of Tool
    - **index.md** - explain what the tool is and what it is used for
    - referance_sheet.md - a printable/link to a printable sheet with basic usage commands and advice, highly summarized
    - docs.md (or folder) - Links to the docs and explaination/guidance for using the docs (& Tips&Tricks)
    - project_use.md - Note which projects use them and roughly how. (Very high-level overview.)
    - tutorials.md (or folder) - Includes or links to tutorials (Text or video) that could guide adoption.
