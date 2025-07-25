---
mode: "agent"
tools: ["vscode", "terminal"]
description: "Analyze and optimize code performance"
---

# Performance Analysis & Optimization

Perform comprehensive performance analysis and optimization of the specified code.

## Target Code Analysis
Analyze the following code components:
${input:targetCode:Specify files, functions, or modules to analyze}

## Performance Analysis Scope

### Execution Time Analysis
- Profile function execution times
- Identify bottlenecks and hot paths
- Measure algorithm complexity (Big O)
- Analyze recursive function performance
- Check loop efficiency and nested iterations

### Memory Usage Analysis
- Monitor memory allocation patterns
- Identify memory leaks
- Analyze object creation and garbage collection
- Check for unnecessary object retention
- Review data structure efficiency

### I/O Performance
- Database query optimization
- File system operations efficiency
- Network request optimization
- Caching strategy evaluation
- Async/await vs callback performance

### Resource Utilization
- CPU usage patterns
- Memory consumption trends
- Network bandwidth utilization
- Disk I/O efficiency
- Concurrent execution performance

## Optimization Strategies

### Algorithm Optimization
- Replace O(n²) algorithms with O(n log n) or better
- Implement efficient data structures (hash maps, trees, etc.)
- Use memoization for expensive computations
- Optimize sorting and searching operations
- Reduce redundant calculations

### Memory Optimization
- Implement object pooling for frequently created objects
- Use weak references where appropriate
- Optimize data structures for memory efficiency
- Implement lazy loading for large datasets
- Reduce memory fragmentation

### Database Optimization
- Add appropriate indexes for frequently queried columns
- Optimize N+1 query problems
- Use database-specific optimization techniques
- Implement query result caching
- Optimize database connection pooling

### Caching Implementation
- Implement multi-level caching strategy
- Use appropriate cache eviction policies
- Add cache warming for frequently accessed data
- Implement distributed caching for scalability
- Monitor cache hit/miss ratios

### Concurrency & Parallelization
- Implement parallel processing where beneficial
- Use appropriate synchronization mechanisms
- Optimize thread pool configurations
- Implement non-blocking I/O operations
- Use async/await patterns effectively

## Performance Testing

### Benchmarking
- Create performance benchmarks for critical paths
- Implement before/after performance comparisons
- Use appropriate profiling tools for the technology stack
- Set performance baselines and targets
- Monitor performance regression

### Load Testing
- Simulate realistic user loads
- Test concurrent user scenarios
- Measure response times under load
- Identify breaking points and bottlenecks
- Test auto-scaling behavior

### Profiling Tools
Use technology-specific profiling tools:
- **Python**: cProfile, py-spy, memory_profiler
- **JavaScript/Node.js**: Chrome DevTools, clinic.js
- **Java**: JProfiler, VisualVM
- **C#**: PerfView, dotTrace
- **Database**: Query execution plans, slow query logs

## Optimization Implementation

### Code Refactoring
- Refactor inefficient algorithms
- Optimize data access patterns
- Implement more efficient data structures
- Remove redundant operations
- Streamline control flow

### Infrastructure Optimization
- Optimize server configurations
- Implement CDN for static assets
- Use appropriate load balancing strategies
- Optimize database configurations
- Implement horizontal scaling where needed

### Monitoring & Alerting
- Set up performance monitoring dashboards
- Implement alerting for performance degradation
- Track key performance indicators (KPIs)
- Monitor resource utilization trends
- Set up automated performance testing

## Deliverables

### Performance Report
1. **Current Performance Baseline**
   - Execution time measurements
   - Memory usage analysis
   - Resource utilization metrics
   - Bottleneck identification

2. **Optimization Recommendations**
   - Prioritized list of optimizations
   - Expected performance improvements
   - Implementation effort estimates
   - Risk assessment for each optimization

3. **Optimized Code**
   - Refactored code with performance improvements
   - Before/after performance comparisons
   - Documentation of changes made
   - Updated tests reflecting optimizations

4. **Performance Testing Suite**
   - Benchmark tests for critical functions
   - Load testing scenarios
   - Performance regression tests
   - Monitoring and alerting configurations

### Implementation Plan
- Phase-by-phase optimization roadmap
- Performance targets and success criteria
- Testing and validation approach
- Rollback plans for each optimization
- Performance monitoring strategy

## Success Metrics
Define clear success criteria:
- Response time improvements (target: X% faster)
- Memory usage reduction (target: X% less memory)
- Throughput improvements (target: X% more requests/second)
- Resource cost reduction (target: X% cost savings)
- User experience improvements (target: X% better scores)

Reference the [General Coding Guidelines](../instructions/general-coding.instructions.md) for optimization best practices.

Generate a comprehensive performance optimization plan with measurable improvements.
