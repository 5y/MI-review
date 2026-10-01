# Human Involvement in Mechanistic Interpretability

## Review artifact

This artifact documents study selection and the final 46-study inventory in the submitted paper. It contains three UTF-8 CSV files. Reviewer identities, private comments, and local file paths are omitted. Historical screening entries are preserved separately from final dispositions.

| File | Rows, excluding header | Contents |
| --- | ---: | --- |
| `source_entries.csv` | 571 | Source entries, duplicate linkage, and anonymous title/abstract tags |
| `study_flow.csv` | 546 | One row per review record, with stage evidence and final disposition |
| `included_studies.csv` | 46 | The studies listed in Table V of the submitted paper |

This is a selection artifact, not a study-level role/method coding matrix. It does not claim to reproduce every qualitative judgment in the synthesis.

## Counts and interpretation

The files reproduce the reported flow:

| Step | Count |
| --- | ---: |
| Source entries | 571 |
| Duplicate entries merged | 26 |
| Unique source-linked records | 545 |
| Record first documented at full text | 1 |
| Review records | 546 |
| No later-stage record | 328 |
| Full-text-stage records | 218 |
| Full-text exclusions | 113 |
| Transition to extraction not completed | 7 |
| Stage 4: extraction and final eligibility | 98 |
| Not included after Stage 4 | 52 |
| Included in synthesis | 46 |

Thus, `571 - 26 + 1 = 546`, `546 - 328 = 218`, `218 - 113 - 7 = 98`, and `98 - 52 = 46`.

The 98 original Stage-4 decisions comprise 55 Include and 43 Exclude. Final Stage-4 dispositions comprise 46 Include, 46 Exclude, and six Background only. Nine historical Includes changed: six to background, one exclusion outside the date window, and two further author exclusions. Those changes appear in the final fields without replacing the original decisions.

The full-text record set contains 202 records present in the full-text sheets and 16 author-confirmed assessments without separate decisions in those sheets. These two evidence types are labeled separately. Presence at a later stage establishes progression, not an unrecorded reviewer vote. `Not recorded`, `No stage record`, and `Transition not completed` do not mean Exclude.

Five other background-only records and four author exclusions did not reach Stage 4; they remain in their recorded flow positions. Consequently, counting every background-only record is not the same as counting the six Stage-4 background dispositions. Nineteen non-corpus records lack a completed historical closure; no closure decision has been invented.

## Identifiers and preparation

`record_id` and `study_id` are preserved review identifiers. Gaps in P-numbering are intentional: IDs are not sequential indices within the 46 included studies. Join the files on `record_id` (or `study_id` for the inventory). `source_entry_id` identifies an individual source row.

Entries were linked by normalized title, DOI, or canonical paper URL. Title matching ignores capitalization, punctuation, spacing, HTML entities, and Unicode diacritics. URL matching normalizes equivalent paper identifiers. `duplicate_of_entry_id` points to the first source entry for the same review record; this is a deduplication link, not proof of retrieval chronology.

Numeric tallies, legends, and instruction rows are not records. Retrieved proceedings or session pages remain source records but are not included studies. Backup sheets do not determine outcomes. A cross-check-only item without a source or Stage-3/4 entry is outside the 546-record flow.

Included titles and reference numbers follow submitted Table V. Source titles retain recorded wording with whitespace normalized, so a source title can differ from the inventory title. Citation keys are linked through the study inventory, not the older trace bibliography field. DOIs and URLs are retained where recorded; blank identifiers do not imply that none exists. Access tokens and tracking parameters are removed from URLs. A DOI link supplies an inventory URL when no direct link is recorded. `scope_exception = Yes` corresponds to the two asterisks in Table V. No new inclusion or role-coding decisions are introduced by this release.

## Column guide

### `source_entries.csv`

- `source`, `source_row`: original source sheet and row for traceability.
- `r1_tag`, `r2_tag`: normalized recorded title/abstract tags. R1/R2 indicate column positions, not consistent reviewer identities across rows.
- `adjudication_tag`, `final_source_tag`: additional decision fields where recorded on the source sheet. They do not replace R1/R2 in agreement calculations.
- `duplicate_of_entry_id`: blank for the first entry in each cluster; otherwise the linked first entry ID.

Decision spelling variants and abbreviations normalize to Include or Exclude. `not sure` and tentative `maybe, lean ...` variants normalize to Maybe. The recorded two-round Include text normalizes to Include. Empty cells become `Not recorded`; nondecision text becomes `Nondecision note` and is not treated as a vote.

### `study_flow.csv`

- `source_entry_count`: number of source rows linked to this record.
- `stage2_logged_outcome`: explicit final source decision, then adjudication, then matching paired tags, in that order. Conflicting or incomplete duplicate-row evidence remains labeled as such.
- `stage2_progression`: whether a later-stage record exists, independent of the source-sheet outcome.
- `stage3_evidence`: `Stage log`, `Author-confirmed review`, or `No stage record`.
- `stage3_logged_tags`: decision tags appearing on the full-text sheets, with sheet/row locators. `prior_R1/R2` are the earlier tags carried on those sheets, not a claim of new independent full-text ratings. `review1/review2` are the later decision fields where present.
- `stage3_logged_outcome`: the last explicit later-review decision where available. On the agreed-paper sheet, matching prior tags supply the logged outcome if no later decision exists. Conflicts across entries remain explicit.
- `flow_disposition`: the mutually exclusive flow position used for the reported counts.
- `stage4_original_decision`: the historical final extraction decision, aggregated across duplicate entries.
- `stage4_final_disposition`: final Include, Exclude, or Background only for records reaching Stage 4; otherwise `No stage record`.
- `final_status`, `final_disposition_basis`: current corpus disposition and its recorded basis. An author exclusion without a supplied detailed rationale is not assigned an invented reason.

### `included_studies.csv`

The inventory supplies `study_id`, `title`, `doi`, `url`, `citation_key`, `paper_reference_number`, and `scope_exception`. It contains exactly the IDs marked Included in `study_flow.csv`.

## Reproducing the basic checks

No additional software package is required. Run this Python 3 snippet from the directory containing the CSV files:

```python
import csv
from collections import Counter

def read(name):
    with open(name, encoding="utf-8", newline="") as f:
        return list(csv.DictReader(f))

source = read("source_entries.csv")
flow = read("study_flow.csv")
included = read("included_studies.csv")
assert len(source) == 571
assert len({r["record_id"] for r in source}) == 545
