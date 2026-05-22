
## References

## Overall assessment

The citation system needs one consistent format, but the reference list itself also needs cleaning, de-duplication, and verification against the actual sources used in the thesis.

---

## Issues to address

### 1. Standardize the in-text citation style across the entire thesis

The in-text citations are currently inconsistent.

In several places, numbered citations are written with parentheses and placed after the punctuation, for example:

> `...build directly on these concepts.(76)`

In a numbered system such as Vancouver, citations should be formatted consistently and placed according to the chosen style rule throughout the thesis.

**Example:**

- `...build directly on these concepts [76].`
- `...analyze the security needs of UAV operations [3].`

**How to fix it:** Choose one referencing style for the full thesis and apply it everywhere. For this thesis, Vancouver-style numbered references are the better fit.

---

### 2. Chapter 2 still uses a different citation logic from the rest of the thesis

Chapter 2 still contains narrative author-year references such as:

> `Schneier (1999)`
> `Mauw and Oostdijk (2005)`

while the rest of the thesis mostly uses numbered references.

**Why this matters:** A thesis should not switch citation systems between chapters. That makes the document look unfinished and weakens academic presentation.

**How to fix it:** Convert Chapter 2 to the same referencing system used in the final thesis.

---

### 3. The bibliography numbering is broken and must be repaired

The extracted reference list contains numbering gaps. In particular, the sequence jumps from 142 to 144 and from 167 to 169.

**How to fix it:** Repair the numbering sequence in the reference manager and re-generate the bibliography so all reference numbers are consecutive.

---

### 4. Several reference entries are incomplete or clearly malformed

Some entries incomplete. For example:

- Reference 25 is only `5G Innovations for Industry Transformation.`
- Reference 36 is effectively a bare URL.

There are also several entries with malformed author metadata, such as entries rendered like:

- `I DJ`
- `Technology NI of S and`
- `Standardization IO for`
- `Council EP and`

**How to fix it:** Open these entries in a reference manager (e.g. [Zotero](https://www.zotero.org/)) and correct the author, title, year, publisher, and URL fields manually.

---

### 5. The reference list contains duplicate or near-duplicate sources

Several vendor and documentation sources appear multiple times in slightly different forms. For example:

- the DJI product specifications page for the UAV appears multiple times
- the DJI Dock 3 specifications page appears multiple times
- several DJI manuals and security documents appear in overlapping forms

**How to fix it:** Merge duplicate references so each distinct source appears once in a clean, complete format unless there is a genuine reason to cite different versions.

---

### 6. Standards references must be checked for exact version consistency

This thesis depends heavily on exact standards versions. At the moment, some standard versions are not fully consistent across chapters.

**Why this matters:** In a clause-level gap analysis, the exact version is part of the method. A mismatch between the bibliography and the chapters weakens reproducibility.

**How to fix it:** Verify that every standards document cited in Chapters 2, 4, 5, and Appendix B appears in the reference list with the exact version, year, and title actually used in the thesis.

---

### 7. Run a full citation-resolution audit

After the bibliography is cleaned, the thesis still needs one final cross-check.

**What to check:**

- every in-text citation points to a real entry in the bibliography
- no bibliography item is uncited unless intentionally retained
- duplicate entries are removed
- broken numbering is fixed
- chapter-specific citation style inconsistencies are gone

---

> It would be a good idea to fix these issues in the reference manager first and only then regenerate the bibliography and the in-text citations. Otherwise the same errors will keep reappearing.
