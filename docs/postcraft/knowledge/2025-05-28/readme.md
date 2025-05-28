# Ragno Ontology

Ragno is a SKOS-based ontology for describing knowledge bases and their graph structures, designed for advanced retrieval and knowledge organization.

## Overview

Ragno extends SKOS (Simple Knowledge Organization System) to model heterogeneous knowledge graphs with various element types that support semantic retrieval and graph-based navigation.

## Core Concepts

- **Element** - Base class for all knowledge graph components (subclass of skos:Concept)
- **Corpus** - A body of knowledge represented as a skos:Collection of Elements
- **Corpuscle** - A conceptual subset of a Corpus, also a skos:Collection

## Element Types

- **Entity** - Named entities serving as knowledge anchors
- **Relationship** - First-class connections between entities
- **Unit** - Semantic units representing independent events
- **Attribute** - Properties of important entities
- **TextElement** - Original text chunks with explicit content
- **CommunityElement** - Insights summarizing graph communities
- **IndexElement** - Search/retrieval structures (embeddings, keywords)

## Key Features

- SKOS integration for concept organization
- PROV-O integration for provenance tracking
- Support for graph algorithms and similarity scoring
- Flexible subtyping through ragno:subType property
- Community-based knowledge organization

## Namespace

`<http://purl.org/stuff/ragno/>`

## Repository

[http://github.com/danja/ragno](http://github.com/danja/ragno)