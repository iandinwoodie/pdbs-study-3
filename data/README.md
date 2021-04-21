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

| owner-id | event   | dog-id | dog-id | dog-id | dog-id | dog-id |
|----------|---------|--------|--------|--------|--------|--------|
| owner-1  | event-2 | dog-1  | dog-2  | dog-3  | dog-4  | dog-5  |
| owner-2  | event-1 | dog-1  | dog-2  | dog-3  | dog-4  | dog-5  |
| owner-2  | event-2 | dog-1  | dog-2  | dog-3  | dog-4  | dog-5  |

