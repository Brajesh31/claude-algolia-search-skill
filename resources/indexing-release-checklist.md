# Algolia Indexing and Search Release Checklist

## Data contract
- [ ] Each record has a stable unique objectID.
- [ ] The record model reflects the user-facing search task, not blindly the source database schema.
- [ ] Searchable attributes are explicit and ordered by importance.
- [ ] Facets and filterable attributes are limited to real product requirements.
- [ ] Required fields, null handling, and normalization are defined.

## Indexing
- [ ] Full reindex and incremental update paths are documented.
- [ ] Batch sizes and retry behavior are tested against current API limits.
- [ ] Partial updates are used only when their merge behavior is understood.
- [ ] Deletes and index swaps have a reviewed recovery plan.
- [ ] Source-of-truth changes are monitored and replayable.

## Frontend and relevance
- [ ] Browser uses a restricted Search API key only.
- [ ] Admin credentials remain server-side.
- [ ] Query, filters, facets, pagination, and URL state are tested.
- [ ] Representative relevance cases pass.
- [ ] Empty, loading, error, and no-result states are usable.
- [ ] Search latency and no-result rates are measured.

## Deployment
- [ ] Settings changes are versioned and reviewed.
- [ ] Staging index or rollback path exists.
- [ ] Index migration and alias/switch strategy is tested where applicable.
- [ ] Monitoring and ownership are assigned.
- [ ] Current Algolia documentation and installed package versions were checked.
