## Introduction
These queries were built for Amazon's internal ETL system to run as automated reports displaying the latest inventory/process metrics on a daily or weekly basis.  For all I know, some of these queries may be running to this day, but the files in this repository are archived, lightly redacted copies of the original queries.  The dates on each file name roughly correspond to when I completed them.

These queries pull, join, and transform data on storage capacity, inventory records, outbound shipments, purchase orders, and more in order to generate new insights, and all of them were originally written to pull data specifically for the warehouse at which I worked.  However, most of the queries are parameterized with wildcards so that the Amazon ETL system could substitute in other warehouse ID codes and thereby send out multiple warehouse-specific reports from a single query.  Several of my queries were thus used more widely within the Amazon fulfillment network, with jobs for those queries running every day and being sent to the operations teams at several different warehouses.

Most of these queries report on inventory quality or storage capacity metrics of some kind.  They mostly use basic operators like SELECT, WHERE, JOIN, GROUP BY, HAVING, CASE WHEN, etc, but some of them involve complex series of joins and/or a high degree of filtering.   
