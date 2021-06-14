# Data

This directory contains the various stages of study data used for analysis.
Brief descriptions of each stage are provided below in order from least to most
modified.

## Raw Data

The raw data (`raw.csv`) is a dump of collected responses from the eletronic
data capture (EDC) platform REDCap. Each row of the raw data represents a user
response for a single event. The survey consisted of two events: (1) gathering
information on the presence of behavior problems for up to 5 dogs and (2)
gathering information on the pursued paths of treatment, if any, for the dogs
that exhibited problematic behavior. From a high level, the layout of this data
can be summarized with the following table:

| owner-id | event-id | dog-1    | dog-2    | dog-3    | dog-4    | dog-5    |
|----------|----------|----------|----------|----------|----------|----------|
| owner-1  | event-1  | dog-data | dog-data | dog-data | dog-data | dog-data |
| owner-1  | event-2  | dog-data | dog-data | dog-data | dog-data | dog-data |
| owner-2  | event-1  | dog-data | dog-data | dog-data | dog-data | dog-data |

## Structured Data

The structured data (`structured.csv`) is a restructuring of the raw data for
ease of analysis. In its new form, the layout of the data can be summarized with
the following table:

| owner-id | dog-id | event-1    | event-2    |
|----------|--------|------------|------------|
| owner-1  | dog-1  | event-data | event-data |
| owner-1  | dog-2  | event-data | event-data |
| owner-2  | dog-1  | event-data | event-data |

Each row represents a complete entry (i.e., both event 1 and event 2 responses)
for a single dog. Incomplete entries were dropped from the data set.

## Manually Cleaned Data

Due to the flexibility afforded by text entry fields, particularly those related
to medication, it was necessary to produce a manually cleaned data set
(`manually-cleaned.csv`). For example, for a certain medication one user may
have provided `{dosage: "10mg", frequency: "1/2 tablet 2x per day"}` while the
expected format for such a response was `{dosage: "5", frequency: "2"}`.
Therefore, certain columns of the data were manually cleaned by researchers
working on the study to ensure appropriate coding of responses. OpenRefine was
used to aid the data cleaning process.

