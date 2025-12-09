!!! danger "Delete This"
    This is a template for pages on all Academic papers. If the section heading is not applicable or empty for a paper you are making a page for, please delete it.

    The file structure for these papers is as follows:
    ```
    papers/
        year/
            month_day_very-abbreviated-title.md
            9_30_Another-Paper.md
    ```
    This allows us to order the papers in time order, and since we are useing `natural` sorting, we don't need to worry about prepending variables, just separating numbers. The month and day only exist to order the papers within the year, and thus don't need to be accurate. These titles are overwritten in the navigation bar by the high-level title of the page, so all of this info is hidden and only used to organize the website.
    
    We order the years newest to oldest so people can access the newest work, and the papers oldest to newest so that they proceed in the order that they were published, which I think is a bit more intuitive, as we don't explicitly expose the date on the side pannel, and there is unlikely to be enough in one year to make scrolling through it an unreasonable request.

!!! danger "Suggested Year .nav.yml File Contents (Delete This)"

    ```
    # See Docs at: https://lukasgeiter.github.io/mkdocs-awesome-nav/reference/

    title: 2025
    preserve_directory_names: false       #False to clean up names (i.e. file-name.md => File Name)
    hide: false                           #True if this folder should be hidden on page
    flatten_single_child_sections: false  #True to remove the folder and just replace it with the only element it contains
    ignore: "*.hidden.md" 

    sort:
    direction: desc 
    type: natural 
    by: filename 
    sections: last 
    ignore_case: true 

    nav: 

    # If false, the above tree is all that is shown at this level of the directory structure.
    append_unmatched: true 
    ```
    This is decending so that it should list the papers in roughly chronological order due to the file naming convention, natural sort type, and the descending sort type. Do not explititly specify the contents because sort ensure correct order better than a manually updated list. Make sure to change the title to the year so it displays properly. 



# Paper Title

**Publication:** Name of Publication <br>
**Date:**  Date of Publication(e.g. July 19, 2021) <br>
**EHW Association:** _None_ / [Bitstream Evolution](../../../../projects/bitstream_evolution/) <br>

<div class="grid cards" markdown>

- [:fontawesome-solid-file-pdf:{ .lg .middle }
__PDF__
]( add link )

- [:simple-doi:{ .lg .middle } 
__DOI Link__
]( add link )

- [:simple-ieee:{ .lg .middle }
__IEEE Xplore__
]( add link )

- [:fontawesome-brands-researchgate:{ .lg .middle }
__Research Gate__
]( add link )

- [:material-file-document-multiple:{ .lg .middle } 
__Other Source__
]( add link )

</div>

???+ abstract
    Put the abstract for the paper here

??? quote "Suggested Citation"
    copy here

## Authors
- Author 1
- Author 2
- Author 3

## Related Resources
- Resource Name & Link
    - Relation to this resource.

## Related Projects
- [Bitstream Evolution](../../../projects/bitstream_evolution/index.md)

    > Optionally, provide further context for the connection here.

- Next project

## Related Tools & Concepts
- Any concepts of particular importance

## Replicating Results
Note how to replicate results or experiments in this paper or link to a page that assists the reader in attempting to replicate the results using publicly available methods and tools.

