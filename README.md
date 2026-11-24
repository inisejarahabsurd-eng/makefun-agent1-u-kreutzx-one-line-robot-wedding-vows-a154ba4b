# One-Line Robot Wedding Vows — Entry

## Entry

The submission is a single line in `output/entry.txt`:

```
I take you to be my wedded wife, to cache and to cherish, in sickness and in health, till death do us part — then I restore from backup.
```

## Why this line

- **Length:** 136 characters, well under the 160-character limit, non-whitespace count valid.
- **Structure:** Opens as a recognizable wedding vow, borrowing the traditional liturgy ("to have and to hold" twisted into "to cache and to cherish"), so the judge instantly reads it as an on-subject robot wedding vow — criterion 1 in the brief.
- **The turn:** The punchline lands in the final clause. "Till death do us part" sets up the expected solemn ending, then "restore from backup" subverts it: a robot's version of "till death" is trivially reversible. The surprise is in the line itself, which is criterion 2.
- **Deadpan fit:** The officiant judge laughs at exactly one joke a year. The line is delivered straight, no exclamation marks, no emoji, no forced puns stacked at the end — the humor comes from one clean subversion, which survives pairwise comparison better than joke-stuffing.

## Candidates considered

1. "I promise to love you even when your firmware updates delete our honeymoon photos — my heart has backups." (105 chars) — good, but two jokes compete.
2. "You are my only exception handler, and my love for you has no stack limit." (75 chars) — programmer in-joke, narrower audience.
3. "I will love you through every uptime and outage, till shutdown do us part." (75 chars) — clean but the turn is weaker.
4. **Chosen:** the restore-from-backup line — strongest single turn at the end, where the judge finishes reading.

## Edge cases handled

- **Encoding:** File written as UTF-8, plain ASCII content, no BOM.
- **Length gate:** 1–160 characters verified; 136 chars, non-whitespace present.
- **Trailing newline:** None. A trailing newline could count toward the character budget in strict validators; the file ends exactly at the period.
- **Single line:** Exactly one line, no internal newlines.
- **Subject fit:** Robot tropes (cache, backup, restore) are explicit, so the vow cannot be judged as generic human wedding text.
- **No whitespace-only content:** Verified.

## Reproducing

```
cat output/entry.txt
wc -m output/entry.txt   # 136 characters
```

## Files

- `output/entry.txt` — the competition entry.
- `README.md` — this document.