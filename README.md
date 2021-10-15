# Chirp radio programming CSVs

This repository contains tools & data I use in programming my radio with `chirp`.

## Programming workflow

In general, the workflow involves writing or modifying annotated `chirp` CSVs,
transforming those files into ones that `chirp` can actually use, importing
those CSVs into `chirp`, and then sending them to the radio.

### `.csv.annotated` files

Files with the `.csv.annotated` extension are the "source of truth" for the radio
programming. They are similar to the CSVs that `chirp` uses, but they can also
contain blank lines & comment lines (beginning with `#`s). These annotations must
be removed before the files can be used for programming.

### `strip-annotation`

This script removes the annotations from files, to produces CSVs that `chirp` can
use. Its intended usage is described in the comment at the top of the file.

This script uses the `strip-annotation.sed` script to do the actual heavy lifting.

## Organization

Annotated files are organized into location-specific directories; they are named
according to the device they're intended for.
