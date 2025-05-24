# Ragno Ontology Overview

## Introduction

Ragno is an RDF/OWL ontology designed for graph-based Retrieval-Augmented Generation (RAG) systems. It models heterogeneous knowledge graphs that support advanced retrieval through dual search mechanisms and graph algorithms.

## Core Concepts

### Element Hierarchy

All Ragno elements extend `ragno:Element`, which is a subclass of `skos:Concept`. This provides:
- Standard concept modeling through SKOS
- Unified properties across all element types
- Integration with existing knowledge organization systems

### Seven Element Types

1. **Entity** (`ragno:Entity`) - Named entities serving as entry points
2. **Relationship** (`ragno:Relationship`) - Connections between entities as first-class nodes
3. **Unit** (`ragno:Unit`) - Semantic units representing independent events
4. **Attribute** (`ragno:Attribute`) - Summarized properties of important entities
5. **TextElement** (`ragno:TextElement`) - Original text chunks with explicit content
6. **CommunityElement** (`ragno:CommunityElement`) - Insights summarizing graph communities
7. **CoreElement** (`ragno:CoreElement`) - Central concepts for community elements

## Key Properties

### Content and Retrieval
- `ragno:content` - Unified text content property
- `ragno:isRetrievable` - Marks elements that can be retrieved
- `ragno:isEntryPoint` - Marks elements for search entry

### Graph Structure
- `ragno:connectsTo` - General connections between elements
- `ragno:inCommunity` - Community membership
- `ragno:hasEmbedding` - Vector representations

### Algorithm Support
- `ragno:hasPPRScore` - Personalized PageRank scores
- `ragno:hasSimilarityScore` - Vector similarity scores
- `ragno:hasWeight` - Edge weights for graph algorithms

## Standards Integration

### SKOS (Simple Knowledge Organization System)
- Elements as concepts with preferred/alternative labels
- Communities as collections
- Semantic relations for navigation

### PROV-O (Provenance Ontology)
- Documents tracked as `prov:Entity`
- Queries modeled as `prov:Activity`
- Source tracking through `prov:wasDerivedFrom`

## Named Graph Architecture

The ontology organizes data into six named graphs:

1. **Ontology Graph** - Schema definitions
2. **Corpus Graph** - Documents and raw text
3. **Decomposition Graph** - Entities, relationships, units
4. **Augmentation Graph** - Attributes, communities, community elements
5. **Enrichment Graph** - Embeddings, semantic edges, text elements
6. **Search Graph** - Queries and retrieval results

## Query Processing

Ragno supports a dual search approach:

1. **Exact Matching** - On entities and core elements
2. **Vector Similarity** - On semantic units, attributes, and community elements

Results are refined through Personalized PageRank and filtered for retrievable elements.

## Implementation

The ontology is expressed in Turtle format and can be used with:
- Standard RDF stores supporting SPARQL 1.1
- Vector databases for embedding storage
- LLM services for content extraction and generation

Namespace: `<http://purl.org/stuff/ragno/>`