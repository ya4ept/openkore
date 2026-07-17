---
title: master
categories:
    - config.txt
    - config.txt|connection
    - Feature request
---

`master <server_name>`

Master server name. Corresponds to server's configuration section name in [servers.txt](../tables/servers.txt.md).

!!! Notes
    --8<-- "template/WillBeAsked.md"

!!! Note "Developer Notes"
    Do not ever change section names in servers.txt since it's used in users' configurations. If you want to update displayed server title, rather implement new optional server option, say **title**, which would be displayed instead of server's name if set, and use it to have up to date server titles.

!!! tip ""
    Category: [config.txt](/cat/config.txt) | [connection](/cat/config.txt-connection) | [Feature request](/cat/feature-request)