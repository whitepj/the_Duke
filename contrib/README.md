# Helpful Scripts

None of the scripts/programs here are part of the actual functioning LMS service.
Rather, they add a level of convenience to the initial preparation.

## Barcode Generation
*barcode.pl* will take an input file containing each barcode input array
separated by newlines, and output a zpl-formatted file to <STDOUT>. Included
within the label are the fields as indicated within the table below.
```
./barcode.pl <input_file>
```

### Tags used
|  | Track | Album | Work | Playlist |
|--|-------|-------|------|----------|
|  |       |       |      |          |
|  |       |       |      |          |

### Example
> [1,["",1990],[[]]]
![Example label](./example.png)

This script reads **__directly__** from the LMS database (rather than through
the LMS daemon via the CLI). Therefore, you will have to run this on the same
machine as the seriver is installed on!

