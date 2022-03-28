## Introduction
These queries were built for Amazon's internal ETL system to run as automated reports displaying daily inventory/process metrics in a digestible format.  For all I know, some of these queries may be running to this day, but the files in this repository are archived, lightly redacted copies of the original queries.  The dates on each file name roughly correspond to when I completed them.

As an analyst, I had access to data tables on storage capacity, inventory records, employee details, purchase orders, and outbound shipments for Amazon fulfillment centers around the world.  All of these queries were originally written in order to pull, join, and transform these data for the specific warehouse at which I worked, but most of them are parameterized with wildcards so that the Amazon ETL system can substitute in the code for any warehouse and get a comparable report.  Several of my queries were thus used more widely within the Amazon fulfillment network, with jobs for those queries running every day for multiple warehouses.

Most of these queries report on inventory quality metrics of some kind.  Below are a few of the topics touched upon in these queries:

### Amnesty
Amnesty refers to inventory that is listed on the Amazon website as in stock but which has physically fallen out of its designated storage location.  Amazon warehouses have processes for collecting amnesty items as well as algorithms for trying to identify the amnesty "source" for each amnesty item (i.e., the physical storage unit from which it fell).  Leaders of individual warehouses want to be able to see how often amnesty source locations are identified, and whether there are specific sections of the building where a disproportionate amount of amnesty is being generated in the first place, so that they can address any process gaps that are causing these defects.  My amnesty_source_defect_found query breaks down amnesty source locations and find rates on a daily basis, replacing what had previously required a manual data pull.  

### Pending Research
(under construction)

### Pallet Receive Error Indicator
(under construction)
