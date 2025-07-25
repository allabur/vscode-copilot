---
description: "Database design and SQL optimization guidelines"
applyTo: "**/*.{sql,py,js,ts}"
---

# Database Instructions

## Database Design Principles
- Follow database normalization rules (1NF, 2NF, 3NF)
- Use meaningful table and column names
- Implement proper primary and foreign key relationships
- Design for scalability and future growth
- Consider denormalization only when performance requires it

## SQL Best Practices
- Use parameterized queries to prevent SQL injection
- Write readable SQL with proper indentation and formatting
- Use explicit column names instead of SELECT *
- Implement proper indexing for frequently queried columns
- Use transactions for data consistency
- Optimize JOIN operations and avoid unnecessary subqueries

## Query Optimization
- Use EXPLAIN/EXPLAIN PLAN to analyze query performance
- Avoid N+1 query problems with proper eager loading
- Use appropriate data types for columns
- Consider query caching for frequently executed queries
- Implement pagination for large result sets
- Use database-specific optimization features

## Connection Management
- Implement connection pooling for better performance
- Handle connection timeouts and retries gracefully
- Close connections properly to prevent resource leaks
- Use read replicas for read-heavy workloads
- Monitor connection pool metrics

## Data Migration
- Write reversible migration scripts
- Test migrations on staging data before production
- Use database migration tools (Alembic, Flyway, etc.)
- Backup data before major migrations
- Plan for zero-downtime migrations

## Security
- Use least privilege principle for database users
- Encrypt sensitive data at rest and in transit
- Regularly update database software and patches
- Implement audit logging for sensitive operations
- Use environment variables for database credentials
- Regularly rotate database passwords
