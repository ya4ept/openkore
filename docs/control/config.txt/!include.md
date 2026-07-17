---
title: "!include"
categories:
  - config.txt
---

`!include <file_name>`

Use this option to include different files as part of the file it's used in. That makes it easier to reuse configurations.


!!! note
    You can use a path that is relative to the file this is used in.

!!! example "Example (config.txt):"

    ```
    !include account.txt
    !include skills/hunterselfskills.txt
    ```

In the example above, if your config.txt is placed in the folder is `C:\Openkore\control`, the files `C:\Openkore\control\account.txt` and `C:\Openkore\control\skills\hunterselfskills.txt` will be included as part of your configuration.
