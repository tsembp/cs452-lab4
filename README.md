# CS452 Lab 4 — MapReduce

A sequential Go implementation of two classic MapReduce applications:

- **Word Count**: counts each word’s occurrences across input documents.
- **Inverted Index**: maps each word to the sorted list of documents that contain it.

## Requirements

- Go

## Run Word Count

```bash
go run cmd/wordcount/main.go master sequential test/data/pg-*.txt
```

Test it with:

```bash
sh ./test/scripts/test-wc.sh
```

## Run Inverted Index

```bash
go run cmd/invertedindex/main.go master sequential test/data/pg-*.txt
```

Test it with:

```bash
sh ./test/scripts/test-ii.sh
```

## Cleanup

MapReduce creates intermediate files named `mrtmp.*`. Remove them with:

```bash
rm mrtmp.*
```