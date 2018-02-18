# DataFusion Benchmarks

Benchmarks comparing the performance of DataFusion with Apache Spark.

## Disclaimer

It is hard to write fair tests at the moment since DataFusion is at such an early stage of development and only has a small subset of the functionality of Apache Spark. 

# Benchmarks

## 1. Generate WKT

This job runs the following SQL against input files of varying sizes.

```sql
SELECT ST_AsText(ST_Point(lat, lng)) FROM locations

```

This benchmark tests the following features:

- Read / Write CSV
- SQL Projection
- User Defined Functions
- User Defined Types

## 2. Sort Locations (work in progress)

This job sorts input files of varying sizes.

This benchmark tests the following features:

- Read / Write CSV
- Sorting

Because DataFusion currently only supports in-memory sorts this benchmark can only be run on small data sets and therefore isn't really a fair test yet.
