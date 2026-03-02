# Entgo Skills

Comprehensive knowledge base for [entgo.io](https://entgo.io) - Go's powerful entity framework for building applications with large data models.

## Overview

Ent is a powerful entity framework for Go that simplifies building and maintaining applications with large data models. It enables modeling database schemas as graph structures using programmatic Go code and static typing via code generation.

## Key Features

- **Type-Safe**: Generated code provides compile-time type safety
- **Graph-Based**: Model data as interconnected entities
- **Code Generation**: Generate clients, builders, and query types from schemas
- **Multiple Storage**: Support for MySQL, PostgreSQL, SQLite, Gremlin
- **Extensible**: Hooks, Privacy, Validation, and custom extensions

## Directory Structure

```
entgo-skills/
├── SKILL.md                    # Main skill definition
├── README.md                   # This file
├── getting-started/            # Quick start guides
├── references/                 # Detailed pattern references
├── best-practices/             # Production best practices
└── troubleshooting/            # Common issues and solutions
```

## Quick Start

```bash
# Install ent tool
go install entgo.io/ent/cmd/ent@latest

# Create schema
go run -mod=mod entgo.io/ent/cmd/ent new User

# Generate code
go generate ./ent
```

```go
// schema/user.go
func (User) Fields() []ent.Field {
    return []ent.Field{
        field.String("name"),
        field.Int("age"),
    }
}

// Usage
user, err := client.User.Create().
    SetName("Alice").
    SetAge(30).
    Save(ctx)
```

## Documentation Map

### Getting Started
- Installation and setup
- First schema creation
- Database connection
- Code generation

### Schema References
- Field types and constraints
- Edge relationships (O2O, O2M, M2M)
- Indexes and constraints
- Mixins for reusable fields

### CRUD References
- Create operations
- Query with predicates
- Update patterns
- Delete operations

### Advanced Topics
- Eager loading
- Graph traversal
- Aggregation
- Transactions
- Hooks
- Privacy policies
- Migrations

## External Resources

- [Official Documentation](https://entgo.io/docs)
- [GitHub Repository](https://github.com/ent/ent)
- [Atlas Migration Tool](https://atlasgo.io)
