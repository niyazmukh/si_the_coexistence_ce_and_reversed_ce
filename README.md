# Data for “The co-existence of the compromise and reversed compromise effects”

This repository contains the trial-level data from Studies 1–3 reported in the manuscript "The co-existence of the compromise and reversed compromise effects" by Niyaz Mukhametzyanov, Yefim Roth, Ido Erev.

The dataset includes **763 participants** recruited through CloudResearch:

- Study 1: 160 participants
- Study 2: 203 participants
- Study 3: 400 participants

The data are stored in long format in:

`Mukhametzyanov, Roth, & Erev 2025 data.csv`

The file contains **37,500 choice observations**: 16,000 from Study 1, 20,300 from Study 2, and 1,200 from Study 3.

## Data structure

In Studies 1 and 2, each participant completed 100 repeated choices in one choice problem, resulting in 100 rows per participant.

In Study 3, each participant completed one choice in each of three supersets. Thus, each participant contributes three rows. The order of the three supersets was randomized.

## Variable dictionary

| Variable | Description | Coding |
|---|---|---|
| `study` | Study number | `1`, `2`, or `3` |
| `age` | Participant age | Age in years |
| `gender` | Self-reported gender | `female`, `male`, `other` |
| `id` | Anonymous participant identifier | Alphanumeric participant ID; constant across all observations from the same participant |
| `trialorder` | Sequential position of the decision within the participant's task | Studies 1–2: `1`–`100`; Study 3: `1`–`3`, indicating the randomized order in which the three supersets were presented |
| `problem` | Choice problem presented on that observation | See the problem-to-superset mapping below |
| `trial` | Trial number within a choice problem | Studies 1–2: `1`–`100`; Study 3: always `1`, because each problem was presented once |
| `trialtime` | Time taken to make the choice | Response time in seconds |
| `selectedoption` | Option selected by the participant | `A`, `B`, `C`, or `D`. For Set ABC the possible values are `A`, `B`, and `C`; for Set BCD they are `B`, `C`, and `D` |
| `optionorder1` | Option presented in the first/top screen position | Option label `A`–`D` |
| `optionorder2` | Option presented in the second/middle screen position | Option label `A`–`D` |
| `optionorder3` | Option presented in the third/bottom screen position | Option label `A`–`D` |
| `attention` | Participant-level result of the separate attention task | `TRUE` = passed the attention task; `FALSE` = did not pass. The same value is repeated across all rows belonging to a participant |

The option positions were randomized in Study 1. In Studies 2 and 3, option positions were fixed within each choice set. Consequently, the three `optionorder` variables record the actual presentation order rather than the abstract identities of the available options.

## Problem and choice-set coding

Odd-numbered problems correspond to **Set ABC**, and even-numbered problems correspond to **Set BCD**.

### Study 1

Superset 8:

- `problem = 1`: Set ABC
- `problem = 2`: Set BCD

### Study 2

Superset 22:

- `problem = 1`: Set ABC
- `problem = 2`: Set BCD

### Study 3

Superset 8:

- `problem = 1`: Set ABC
- `problem = 2`: Set BCD

Superset 22:

- `problem = 3`: Set ABC
- `problem = 4`: Set BCD

Superset 140:

- `problem = 5`: Set ABC
- `problem = 6`: Set BCD

## Additional notes

The dataset contains no missing values in the variables listed above.

The `attention` variable records performance on the separate attention task and is participant-level rather than trial-level; its value is therefore repeated across that participant's choice observations.

For full descriptions of the experimental designs, payoff distributions, procedures, and preregistrations, see the manuscript and its Supplementary Materials.
