# Appendix: NodeRAG Background and Terminology Mapping

## NodeRAG Paper

Ragno is based on the NodeRAG framework described in:

> Xu, T., et al. "NodeRAG: Hierarchical Retrieval-Augmented Generation with Heterogeneous Graph Nodes"

NodeRAG introduced a graph-based RAG approach using heterogeneous nodes and a dual search mechanism combining exact matching with vector similarity.

## Terminology Evolution

The Ragno ontology refines NodeRAG terminology for clarity:

| NodeRAG Term | Symbol | Ragno Term | Rationale |
|--------------|--------|------------|-----------|
| Node | - | `ragno:Element` | Base class extending `skos:Concept` |
| Text | T | `ragno:TextElement` | Explicit content property |
| Semantic Unit | S | `ragno:Unit` | Simplified naming |
| High-Level Element | H | `ragno:CommunityElement` | Emphasizes community context |
| High-Level Overview | O | `ragno:CoreElement` | Indicates central importance |
| Entity | N | `ragno:Entity` | Unchanged |
| Relationship | R | `ragno:Relationship` | Unchanged |
| Attribute | A | `ragno:Attribute` | Unchanged |

## Key Adaptations

### Standards Integration
- NodeRAG's custom node types → SKOS concepts
- Custom graph structure → RDF named graphs
- Implicit provenance → Explicit PROV-O tracking

### Property Unification
- Various content fields → Single `ragno:content` property
- Multiple retrieval flags → Boolean properties
- Custom scoring → Standard datatype properties

### Graph Organization
NodeRAG's pipeline stages map to named graphs:
1. Decomposition → Decomposition Graph
2. Augmentation → Augmentation Graph  
3. Enrichment → Enrichment Graph
4. Query/Retrieval → Search Graph

## Algorithm Preservation

Ragno maintains NodeRAG's core algorithms:
- Dual search (exact + similarity)
- Shallow PPR (2 iterations)
- HNSW for semantic edges
- Community detection for augmentation