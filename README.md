# Evolvable Hardware Community Website

The official website for the evolvable hardware research community, built with MkDocs and Material theme.

## Contributing

If you want to contribute to the research, pick a project that you find interesting and navigate to it's webpage.

If you want to contribute to this site, please make the change you were suggesting to the website and file a pull request. You can also `Contact Us` with the information in the website if you don't see any action taken arround it. The general steps are described below:

1. Clone This Repository (`git clone`)
2. Create a locally hosted version of that website
    - `cd /directory/of/cloned/repo`
    - `mkdocs serve`, open povided url in a web browser.
3. Make your changes to the website in the /docs directory. Whenever you save a file, the changes will be shown on your locally hosted website
4. File a pull-request in GitHub.

## Templates
The templates directory has numerous templates for various uses. Please copy these files when trying to add something to the website. These files contain general guidance for how to edit them, and you should stick to that format whenever reasonable.

- **tool_template (folder)**
    - This is a folder providing a general structure for what a tool or platform of slightly varying tools (like hardware IC platforms) should look like on the site.
    - The `variants` directory can be removed if you are not a platform and don't have any notable variants.
- **paper.md**
    - This provides a template for all papers on the site, be it ours or external. If a section isn't used, it can be removed.
- **misc_info.md**
    - A scratch file containing text or icons we may want to reuse.
