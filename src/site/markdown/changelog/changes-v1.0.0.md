# Changelog v1.0.0

Version 1.0.0 of CLAVIN represents a departure from the experimental 0.4.x API and a return to the familiar 0.3.x API. 0.4.x introduced an unnecessary amount of complexity and abstraction into the codebase, and a major refactoring of the core algorithm resulted in a significant reduction in resolution accuracy. By reverting to the 0.3.x codebase for the 1.0.0 release, the API is far simpler to use and algorithmic performance has returned to its previous high levels.

This list details most of the major and minor changes made to the CLAVIN API:

- Extensive code cleanup and additional documentation
- Removed coordinate extraction classes; these capabilities will be re-added to a future release
- Reverted from `PlaceReference` and `ResolutionContext` in favor of `ResolvedLocation`
- Updated documentation info for website generated by **Maven Site** plugin
- Moved everything to `com.bericotech` namespace for distribution via **Maven Central**
- Algorithmic heuristic tests are no longer *integration tests*
- Data model again mirrors **GeoNames.org** gazetteer format
- Returned to a direct dependency on **Lucene** document index for resolution
- Returned to a **Lucene** indexing strategy where each alternateName, etc. for a location is stored as a separate entry; this is essential for the resolution algorithm to achieve high accuracy/recall
- Removed customizable weighting strategies for resolution algorithm; tuning should only be attempted through the `maxHitDepth`, `maxContextWindow`, and `fuzzy` parameters
- Return of `IndexDirectoryBuilder` replacing previous abstractions
- Major improvements to packaging and distribution of releases, now via **Maven Central**
- Better alignment with standard Java coding conventions

