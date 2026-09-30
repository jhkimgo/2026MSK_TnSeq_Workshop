# Part 4 Input Files

This folder contains the example input files required for the Part 4 Circos visualization workflow.

## Custom Karyotype File

`Example_Karyotype.txt` defines the chromosome information used for Circos visualization.

The karyotype file follows this format:

```text
chr - SEQUENCE_ID LABEL START END COLOR
```

For the example dataset:

```text
chr - NC_002516.2 Chromosome 0 6264404 black
```

where:

- `NC_002516.2` = Sequence ID
- `Chromosome` = Display label
- `0` = Start position
- `6264404` = Genome length
- `black` = Ideogram color

## How to Find the Sequence ID and Genome Length

The Sequence ID and genome length can be obtained directly from the GFF annotation file.

Open the GFF file and look for the `##sequence-region` line near the beginning of the file.

For example:

```text
##sequence-region NC_002516.2 1 6264404
```

This line indicates:

- **Sequence ID:** `NC_002516.2`
- **Genome start:** `1`
- **Genome length:** `6264404`

The corresponding Circos karyotype line is:

```text
chr - NC_002516.2 Chromosome 0 6264404 black
```

The **Sequence ID must exactly match** the sequence ID used in the GFF and other input files. The display label (`Chromosome`) can be changed as desired.

For a different genome, replace `SEQUENCE_ID` and `END` with the corresponding sequence ID and genome length obtained from its GFF file.

## How to Create the Karyotype File in Galaxy

1. Click **Upload Data**.
2. Select **Paste/Fetch data**.
3. Paste the karyotype line into the text box.

```text
chr - NC_002516.2 Chromosome 0 6264404 black
```

4. Enter a file name, for example:

```text
Example_Karyotype.txt
```

5. Set the datatype to `txt`.
6. Upload the file.
7. Select the uploaded file as the **Custom Karyotype** input in the Part 4 Circos workflow.
