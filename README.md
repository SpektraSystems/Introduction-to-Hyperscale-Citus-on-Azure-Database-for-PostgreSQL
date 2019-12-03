# Introduction-to-Hyperscale-Citus-on-Azure-Database-for-PostgreSQL

Azure Database for PostgreSQL is a managed service that you use to run, manage, and scale highly available PostgreSQL databases in the cloud. These instructions will show you how to create an Hyperscale (Citus) on Azure Database for PostgreSQL server group using the Azure portal. You'll explore distributed data: sharding tables across nodes, ingesting sample data, and running queries that execute on multiple nodes.

## Overview 

The Hyperscale (Citus) on Azure Database for PostgreSQL is worry-free Postgres that is built to scale out. It distributes (shards), data and queries in a cluster of multiple machines. As an extension (rather than a fork), Hyperscale (Citus) supports new PostgreSQL releases, allowing users to benefit from new features while maintaining compatibility with existing PostgreSQL tools. It solves 2 main problems of performance and scalability with existing workloads. Along with the above, Hyperscale (Citus) also manages the database for you. It provides High Availability, Backups, Monitoring, Alerts and other bells and whistles that are typically part of a PAAS (Platform as a Service) offering.

## Architecture

Every cluster has one special node called the coordinator (the others are known as workers). Applications send their queries to the coordinator node which relays it to the relevant workers and accumulates the results.
For each query, the coordinator either routes it to a single worker node, or parallelizes it across several depending on whether the required data lives on a single node or multiple. Below are some scenarios on how Hyperscale (Citus) distributes your queries across multiple workers.

