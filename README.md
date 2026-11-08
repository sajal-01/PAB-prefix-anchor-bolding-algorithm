# PAB – Prefix-Anchor Bolding Algorithm for faster reading

This notebook converts text (from a **text PDF, a scanned PDF, an image, a .txt file, or pasted text**) so that the
**leading letters of every word are bold**, then rebuilds a **single combined PDF** where the original text is replaced page by page.

**Algorithm: PAB (Prefix-Anchor Bolding)**

| Word length | Letters bolded (from the left, always continuous) |
|---|---|
| 1 | 1 (whole word) |
| 2 | 1 |
| 3 | 2 |
| 4 | 2 |
| 5 | 2 or 3 |
| 6 | 3 |
| 7+ | 4 or 5 |

Where two options exist, the longer one is used **if the bold prefix is itself a common word / common prefix** (e.g. **high**lighted, **over**come); otherwise a length-based default is used. Punctuation is never bolded.

Run the cells from top to bottom.
