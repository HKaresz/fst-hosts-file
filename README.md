# fst-hosts-file
The repository contains the converted file from StevenBlack's hosts file into finite-state transducer (FST) format to provide compact, fast membership lookups.

It is updated daily once the source hosts file is updated.

The blockfile.meta binary file contains the following information, each section is expressed as little-endian uint32:
- header (static)
- version (unix timestamp when the fst file was created)
- length of the fst file
- CRC32 of the fst file

The metadata file provides a convenient way to check whether the fst file contains any update.
