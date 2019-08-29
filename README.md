# Comparison of AWS Aurora MySQL & PostgreSQL

[Amazon Aurora](https://aws.amazon.com/rds/aurora/) is an AWS RDS database engine with two editions: MySQL and PostgeSQL.

Amazon often headlines both editions without distinction as "Aurora" ([example](https://aws.amazon.com/blogs/aws/amazon-aurora-backtrack-turn-back-time/)), but there are significant differences between the two. This is a convenient reference to understand their features and avoid confusion over the generic "Aurora" label.

## Comparison

Dates of feature support are given to provide a sense of priority and timing.

| | MySQL | PostgreSQL |
|---|:-:|:-:|
| General availability | [2015-07-27](https://aws.amazon.com/blogs/aws/now-available-amazon-aurora/) | [2017-10-24](https://aws.amazon.com/blogs/aws/now-available-amazon-aurora-with-postgresql-compatibility/) |
| Zero-downtime RDS migration | [2015-07-27](https://aws.amazon.com/blogs/aws/now-available-amazon-aurora/) | [2018-01-22](https://aws.amazon.com/about-aws/whats-new/2018/01/announcing-amazon-aurora-postgresql-read-replica-for-amazon-rds-for-postgresql/) |
| Encryption at rest | [2015-12-07](https://aws.amazon.com/blogs/aws/new-encryption-at-rest-for-amazon-aurora/) | [2017-10-24](https://aws.amazon.com/blogs/aws/now-available-amazon-aurora-with-postgresql-compatibility/) |
| Cross-region replication | [2016-06-01](https://aws.amazon.com/blogs/aws/new-cross-region-read-replicas-for-amazon-aurora/) | No |
| Reader endpoint | [2016-09-08](https://aws.amazon.com/blogs/aws/new-reader-endpoint-for-amazon-aurora-load-balancing-higher-availability/) | [2017-10-24](https://aws.amazon.com/blogs/aws/now-available-amazon-aurora-with-postgresql-compatibility/) |
| Asynchronous lambda procedures | [2016-10-18](https://aws.amazon.com/blogs/aws/amazon-aurora-update-call-lambda-functions-from-stored-procedures-load-data-from-s3/) | No |
| T2/T3 instances (burstable instances) | [2016-11-23](https://aws.amazon.com/blogs/aws/use-amazon-aurora-for-dev-test-workloads-with-new-t2-medium-db-instance-class/) | No |
| IAM database authentication | [2017-04-24](https://aws.amazon.com/blogs/security/manage-access-to-your-rds-for-mysql-and-amazon-aurora-databases-using-aws-iam/) | [2018-11-08](https://aws.amazon.com/about-aws/whats-new/2018/11/amazon-aurora-postgresql-supports-iam-authentication/) |
| S3 export | [2017-06-01](https://aws.amazon.com/about-aws/whats-new/2017/06/amazon-aurora-can-export-data-into-amazon-s3/) | No |
| Fast cloning | [2017-08-30](https://aws.amazon.com/blogs/aws/amazon-aurora-fast-database-cloning/) | [2018-04-10](https://aws.amazon.com/about-aws/whats-new/2018/04/amazon-aurora-with-postgresql-compatibility-supports-fast-database-cloning/) |
| Auto scaling replicas | [2017-11-17](https://aws.amazon.com/about-aws/whats-new/2017/11/amazon-aurora-now-supports-auto-scaling-for-aurora-replicas/) | [2018-08-16](https://aws.amazon.com/about-aws/whats-new/2018/08/amazon-aurora-with-postgresql-compatibility-supports-auto-scaling-replicas/)
| Synchronous lambda procedures | [2017-12-11](https://aws.amazon.com/about-aws/whats-new/2017/12/amazon-aurora-with-mysql-compatibility-natively-supports-synchronous-invocation-of-aws-lambda-functions/) | No |
| Backtrack (fast in-place restore) | [2018-05-10](https://aws.amazon.com/blogs/aws/amazon-aurora-backtrack-turn-back-time/) | No |
| Publish logs to CloudWatch | [2018-05-23](https://aws.amazon.com/about-aws/whats-new/2018/05/amazon-aurora-publishes-general-slow-query-and-error-logs-to-amazon-cloudwatch/) | No | 
| Performance insights (advanced database monitoring) | [2018-08-06](https://aws.amazon.com/about-aws/whats-new/2018/08/performance-insights-is-available-for-amazon-aurora-with-mysql-compatibility/) | [2018-07-18](https://aws.amazon.com/about-aws/whats-new/2018/04/rds-performance-insights-on-rds-for-postgresql/)
| Serverless (automatic startup/shutdown) | [2018-08-09](https://aws.amazon.com/blogs/aws/aurora-serverless-ga/) | [2019-07-09](https://aws.amazon.com/about-aws/whats-new/2019/07/amazon-aurora-with-postgresql-compatibility-supports-serverless/) |
| Parallel query (storage-level query processing) | [2018-09-28](https://aws.amazon.com/blogs/aws/new-parallel-query-for-amazon-aurora/) | No |
| Custom endpoints | [2018-11-22](https://aws.amazon.com/about-aws/whats-new/2018/11/amazon-aurora-simplifies-workload-management-with-custom-endpoints/) | [2018-11-22](https://aws.amazon.com/about-aws/whats-new/2018/11/amazon-aurora-simplifies-workload-management-with-custom-endpoints/) |
| Global database (fast cross-region replication) | [2018-11-27](https://aws.amazon.com/about-aws/whats-new/2018/11/announcing-amazon-aurora-global-database/) | No |
| Query Plan Management (control query plan changes) | No | [2018-12-19](https://aws.amazon.com/about-aws/whats-new/2018/12/amazon-aurora-postgresql-compatibility-adds-query-plan-management/) |
| Performance insights counter metrics | [2019-02-20](https://aws.amazon.com/about-aws/whats-new/2019/02/Performance-Insights-Counter-Metrics-MS-PG-AMS/) | [2018-12-17](https://aws.amazon.com/about-aws/whats-new/2018/12/amazon-rds-performance-insights-supports-counter-metrics-for-aurora-postgresql/)
| Replication with native databases | Yes | [2019-03-28](https://aws.amazon.com/about-aws/whats-new/2019/03/amazon-aurora-with-postgresql-compatibility-supports-logical-replication/) |
| Import S3 backups (e.g. fast RDS migration) | [2019-04-18](https://aws.amazon.com/about-aws/whats-new/2019/04/amazon_aurora_and_amazon_rds_enable_faster_migration_from_mysql_57_databases/) | No |
| Data API (JSON API) | [2019-05-30](https://aws.amazon.com/blogs/aws/new-data-api-for-amazon-aurora-serverless/) | No |
| Multi-Master | [2019-08-08](https://aws.amazon.com/about-aws/whats-new/2019/08/amazon-aurora-multimaster-now-generally-available/) | No |
| Instance families | t2, t3, r3, r4, r5 | t3<sup>[1](#footnote-1)</sup>, r4, r5 |
| Maximum storage | 64 TB | 64 TB |
| Continuous incremental backups | 1-35 days | 1-35 days |
| Minimum cost (on-demand) | [$30/month](https://aws.amazon.com/rds/aurora/pricing/) | [$209/month](https://aws.amazon.com/rds/aurora/pricing/) |
| Version upgrade path | Supported | Supported for minor versions only<sup>[2](#footnote-1)</sup> |

<sup><a name="footnote-1">1.</a> Only t3.medium.</sup>

<sup><a name="footnote-2">2.</a> [Documention](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/USER_UpgradeDBInstance.Upgrading.html) claims support, but AWS Support has confirmed that is not the case: "The documentation might be confusing in the description, unfortunately the upgrade of an existing Aurora PostgreSQL instance version 9.6.x to version 10.x, is still not supported."</sup>

## Contribution

Please contribute a PR to fix incomplete/inaccurate information.
