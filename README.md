# AssisTV

Knowledge engineering system for television content management. Built as a university project.

## Overview

AssisTV retrieves information about TV content from multiple sources and represents it using **knowledge engineering** and **ontologies**, enabling structured querying over heterogeneous data.

## Architecture

```
TV Data Sources → Relational DB → R2RML Mapping → OWL Ontology → SPARQL queries
                                       ↑
                                  Ontop (OBDA)
```

The system uses **OBDA (Ontology-Based Data Access)** via [Ontop](https://ontop-vkg.org/): a relational database is exposed as a virtual knowledge graph through an OWL ontology, without physically migrating data. SPARQL queries are translated to SQL at runtime.

## Contents

| File / Folder | Description |
|---|---|
| `AssisTV owl.owl` | OWL ontology defining TV content concepts and relations |
| `AssisTV.obda` | Ontop OBDA mapping configuration |
| `OnTop/AssisTV-mapping R2RML.ttl` | R2RML mapping (database schema → ontology) |
| `OnTop/query(ontop).txt` | SPARQL queries |
| `assistvturtle/` | Ontology in Turtle format |
| `Interfaccia Web/` | Web interface for querying the knowledge graph |
| `Specifiche/` | Project specifications |
| `LODE Documentazione AssisTV.mhtml` | Auto-generated LODE ontology documentation |
| `Relazione di progetto (AssisTV).pdf` | Full project report |

## Tech Stack

- **OWL 2** (Web Ontology Language): knowledge representation
- **Ontop**: OBDA / virtual knowledge graph engine
- **R2RML**: relational-to-RDF mapping language
- **SPARQL**: query language for the knowledge graph
- **Turtle** (`.ttl`): RDF serialization format
- **HTML/CSS**: web interface

## Run

1. Open `AssisTV owl.owl` in [Protégé](https://protege.stanford.edu/)
2. Load the Ontop plugin and configure with `AssisTV.obda`
3. Run SPARQL queries from `OnTop/query(ontop).txt`

---

*University project, Knowledge Engineering / Semantic Web, 2021*
