## 0.6.0 / 2015-10-28

BREAKING CHANGES:
* The digest_text mapping metric has been removed, now included in all digest metrics (PR #50)
* Flags for timing metrics have been removed, now included with related counter flag (PR #48)

* [FEATURE] New collector for metrics from information_schema.processlist (PR #34)
* [FEATURE] New collector for binlog counts/sizes (PR #35)
* [FEATURE] New collector for performance_schema.{file_summary_by_event_name,events_waits_summary_global_by_event_name} (PR #49)
* [FEATURE] New collector for information_schema.tables (PR #51)
* [IMPROVEMENT] All collection methods now have enable flags (PR #46)
* [IMPROVEMENT] Consolidate performance_schema metrics flags (PR #48)
* [IMPROVEMENT] Removed need for digest_text mapping metric (PR #50)
* [IMPROVEMENT] Update docs (PR #52)

## 0.5.0 / 2015-09-22

* [FEATURE] Add metrics for table locks
* [BUGFIX] Use uint64 to prevent int64 overflow
* [BUGFIX] Correct picsecond times to correct second values

## 0.4.0 / 2015-09-21

* [CHANGE] Limit events_statements to recently used
* [FEATURE] Add digest_text mapping metric
* [IMPROVEMENT] General refactoring

## 0.3.0 / 2015-08-31

BREAKING CHANGES: Most metrics have been prefixed with Prometheus subsystem names
                  to avoid conflicts between different collection methods.

* [BUGFIX] Separate slave_status and global_status into separate subsystems.
* [IMPROVEMENT] Refactor metrics creation.
* [IMPROVEMENT] Add support for performance_schema.table_io_waits_summary_by_table collection.
* [IMPROVEMENT] Add support for performance_schema.table_io_waits_summary_by_index_usage collection.
* [IMPROVEMENT] Add support for performance_schema.events_statements_summary_by_digest collection.
* [IMPROVEMENT] Add support for Percona userstats output collection.
* [IMPROVEMENT] Add support for auto_increment column metrics collection.
* [IMPROVEMENT] Add support for `SHOW GLOBAL VARIABLES` metrics collection.

## 0.2.0 / 2015-06-24

BREAKING CHANGES: Logging-related flags have changed. Metric names have changed.

* [IMPROVEMENT] Add Docker support.
* [CHANGE] Switch logging to Prometheus' logging library.
* [BUGFIX] Fix slave status parsing.
* [BUGFIX] Fix truncated numbers.
* [CHANGE] Reorganize metrics names and types.

## 0.1.0 / 2015-05-05

* Initial release
