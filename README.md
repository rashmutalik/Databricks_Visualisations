# Databricks_Visualisations


---

## Overview

This section covers the analytical visualisation layer built on top of the `flights_clean` Delta table. Three visualisations were created inside Databricks to uncover patterns in 2015 international flight data between the US and the rest of the world.

---

## Visualisations

### 1. Net Flow Bar Chart

Joins outbound and inbound flight counts per country and calculates the directional difference (net flow) between the US and every other country.

**Key insights:**
- Positive values = US sends more flights out (e.g. Caribbean islands)
- Negative values = More flights arrive into the US (e.g. Mexico, Colombia)
- Near zero = Balanced, reciprocal travel relationship

---

### 2. Route Symmetry Scatter Plot

Self-joins the Delta table to compare forward vs reverse flight counts for every bidirectional route, calculating an imbalance score for each pair.

**Key insights:**
- Routes on the diagonal = balanced demand in both directions
- Routes off the diagonal = one direction is underserved, pointing to potential airline revenue opportunities

---

### 3. Volume Bucket Pie Chart

Segments all routes into three categories — High (1000+), Medium (100–999) and Low (<100) — to understand how traffic is distributed across the network.

**Key insights:**
- Reveals whether the network is driven by a few mega-routes or spread across many smaller connections
- Useful for understanding where to focus operational and commercial resources

---

## What These Three Charts Tell Together

| Chart | Question Answered |
|---|---|
| Net Flow Bar Chart | Which countries drive directional imbalance? |
| Route Symmetry Scatter Plot | Which specific routes are lopsided? |
| Volume Bucket Pie Chart | How is the overall network structured? |

Together they build a complete analytical narrative — from network structure, to route efficiency, to country-level imbalance.
