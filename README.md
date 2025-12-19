# Ownership Concentration in Skilled Nursing Facilities (CMS)

This project analyzes ownership concentration and organizational control within U.S. Skilled Nursing Facilities (SNFs) using publicly available data from the Centers for Medicare & Medicaid Services (CMS).

Rather than focusing on surface-level descriptive statistics, the analysis examines how facility ownership is distributed across affiliation entities, revealing structural concentration patterns within the long-term care sector.

---

## Dataset

**Source:** CMS Open Data  
**API Endpoint:**  
https://data.cms.gov/data-api/v1/dataset/5f2c306f-3b1c-42cd-b037-187b2ce22126/data

**Dataset:** Skilled Nursing Facility (SNF) Enrollments  
**Access Method:** Direct API pull via `pandas.read_json()`

The dataset includes enrollment, ownership classification, organizational structure, and affiliation identifiers for Medicare-participating SNFs.

---

## Research Focus

This project addresses the following questions:

- How concentrated is SNF ownership across affiliation entities?
- Do a small number of entities control a disproportionate share of facilities?
- How does ownership concentration vary across organizational structures (e.g., corporations vs LLCs)?
- What does affiliation-based control reveal about market power in long-term care?

---

## Methodology

1. **Data Ingestion**
   - API-based retrieval of CMS enrollment data
   - Schema normalization and cleaning

2. **Structural Analysis**
   - Facility counts by state
   - Ownership classification (proprietary vs nonprofit)
   - Legal organization structure

3. **Ownership Concentration**
   - Aggregation of facilities by `affiliation_entity_id`
   - Ranking entities by number of facilities controlled
   - Computation of cumulative ownership share

4. **Visualization**
   - Bar charts for structural context
   - Cumulative concentration curve illustrating ownership dominance

---

## Key Insight

A relatively small number of affiliation entities control a disproportionately large share of Skilled Nursing Facilities, indicating meaningful ownership concentration within the sector. This concentration raises important questions about competition, regulatory oversight, and private equity involvement in long-term care.

---

## Notes & Limitations

- The analysis uses the first 1,000 records returned by the CMS API.
- Affiliation entity identifiers may represent intermediate ownership layers rather than ultimate beneficial owners.
- Results are intended to highlight structural patterns rather than provide exhaustive enumeration.

---

## Tools & Libraries

- Python
- pandas
- matplotlib

---

## License

This project uses publicly available government data and is intended for research and educational purposes.
