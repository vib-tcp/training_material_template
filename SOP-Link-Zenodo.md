
# SOP: Get a DOI by syncronizing with Zenodo Metadata

## Purpose

This SOP ensures that the course instance will have a DOI linked to the Training and Confereces Zenodo community with the release metadata consistent across GitHub and Zenodo.

## Scope

Applies to:

- [CITATION.cff](CITATION.cff)

- [zenodo.json](zenodo.json)

- GitHub releases and tags

## Source of Truth Rules

For each release, define values once and copy exactly to both metadata files where relevant.

- Title: must be the same present in registration page at [Training and Conferences](https://www.vibtrainingandconferences.be/#/) and in [CITATION.cff](./CITATION.cff) and [zenodo.json](./zenodo.json).

- Version: use the YYYYMMDD format for consistance and easy identification. You can also, when relevant, include the city. 
e.g.: V.20260812, V20260812_Gent

- License: must match in both files. Advised license is [CCBY 4.0 interntional](https://creativecommons.org/licenses/by/4.0/deed.en)

- Type: keep as lesson in both files.

- Keywords: same concepts in both files.

- People metadata: names, affiliations, ORCIDs, and ordering should match in README, Zenodo and Citation files. Citation file is the main one used to create the citation in Zenodo. In case there is an error in the Citation file, this can be later updated directly in Zenodo.

## Release Lifecycle

### 1. Pre-release metadata update (before tagging)

1. Update [CITATION.cff](./CITATION.cff):
	- title
	- version
	- date-released (YYYY-MM-DD)
	- identifiers version (V.yyyymmdd)
	- authors/contact (if changed)
	- keywords

2. Update [zenodo.json](zenodo.json):
	- title
	- version
	- description
	- creators/contributors
	- keywords

3. Remove placeholders and typos in both files.

4. Commit these updates to the default branch.

### 2. Create release on GitHub

1. Create a GitHub tag using the exact version used in metadata in the format V.yyyymmdd as suggested.

2. Create the GitHub release from that tag. Explain in the release what updates were made in relation to the previous version of the lesson. 


### 3. Zenodo record creation and DOI sync (post-release)

1. Wait for Zenodo to archive the new GitHub release.

2. Open the Zenodo record and collect:
	- version-specific DOI
	- final citation text

3. Update [README.md](./README.md):
	- Include the DOI in the lesson overview
    - Incliude the citation in dedicate part of the lesson overview

4. If Zenodo metadata was edited manually in Zenodo, mirror those edits back into [zenodo.json](zenodo.json).

5. Commit with a clear message, for example:
	- Update DOI and Citation after sync in zenodo for the latest course instance.

### 4. Validation gate (mandatory)
Before closing the release, verify all checks below:

1. version in [CITATION.cff](CITATION.cff) equals version in [zenodo.json](zenodo.json) equals GitHub tag.
2. title and license match in both metadata files.
3. names, affiliations, and ORCIDs are valid and consistent.

## Quick Checklist (Copy/Paste for Release PR)
- [ ] Updated [CITATION.cff](CITATION.cff) fields: title, version, date-released, identifiers, people, keywords.
- [ ] Updated [zenodo.json](zenodo.json) fields: title, version, description, people, keywords.
- [ ] Metadata commit merged before tagging.
- [ ] GitHub tag and release created.
- [ ] Zenodo record generated and DOI captured.
- [ ] DOI synced back to [CITATION.cff](CITATION.cff).
- [ ] Final cross-check completed.

## Notes for This Repository
- Keep repository URL consistent across metadata files.
- Keep the same ordering of contributors where possible.
- Replace all placeholder values before each official release.