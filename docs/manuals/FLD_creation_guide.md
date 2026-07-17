---
title: FLD_Creation_Guide
---

## How to extract custom maps and create FLD file
(note: short version)

- 1\. Extract the map (gat and rsw)
- 2\. Copy both to the root of your OpenKore folder
- 3\. Execute script: `fields\tools\gat_to_fld2.pl` (You will find the created .fld data in the root of your OpenKore folder.)
- 4\. You can pack the files into a gz archive or skip this step
- 5\. Copy created **.fld2** data to `OpenKore\fields`
- 6\. Enjoy

You can either execute the script by using:

- a perl interpreter of choice
- the perl interpreter kore uses: start.exe

1.  cd to kore\'s root folder;
2.  run the following command:

` C:\Openkore\start.exe ! .\fields\tools\gat_to_fld2.pl`

**Note:** in this example the root folder was: C:\\Openkore, yours can be different depending on where you have installed OpenKore.

## See also
[Field file format](Field_file_format.md)
