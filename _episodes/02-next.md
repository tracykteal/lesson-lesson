---
title: "Next"
teaching: 0
exercises: 0
questions:
- "How to write a query"
objectives:
- "Write a query."
keypoints:
- "Queries are questions."
---

## Writing my first query

Let's start by using the **surveys** table. Here we have data on every
individual that was captured at the site, including when they were captured,
what plot they were captured on, their species ID, sex and weight in grams.

Let’s write an SQL query that selects only the year column from the
surveys table.

    SELECT year
    FROM surveys;

We have capitalized the words SELECT and FROM because they are SQL keywords.
SQL is case insensitive, but it helps for readability, and is good style.

If we want more information, we can just add a new column to the list of fields,
right after SELECT:

    SELECT year, month, day
    FROM surveys;

Or we can select all of the columns in a table using the wildcard *

    SELECT *
    FROM surveys;

### Unique values

If we want only the unique values so that we can quickly see what species have
been sampled we use `DISTINCT`

    SELECT DISTINCT species_id
    FROM surveys;

If we select more than one column, then the distinct pairs of values are
returned

    SELECT DISTINCT year, species_id
    FROM surveys;