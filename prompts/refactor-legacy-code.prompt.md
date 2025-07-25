---
mode: "agent"
tools: ["vscode"]
description: "Refactor legacy code to modern patterns and best practices"
---

# Legacy Code Refactoring

Analyze and refactor legacy code to modern patterns, improving maintainability, performance, and security.

## Target Code Analysis
Specify the code that needs refactoring:
${input:targetFiles:Enter file paths or modules to refactor}

## Refactoring Scope
- **Language/Framework**: ${input:language:Programming language (python, javascript, java, csharp, etc.)}
- **Refactoring Type**: ${input:refactoringType:Type of refactoring (architecture, patterns, performance, security)}
- **Modernization Target**: ${input:modernTarget:Target modern version (Python 3.11, ES2023, .NET 8, etc.)}

## Analysis Areas

### Code Quality Assessment
- Code complexity analysis (cyclomatic complexity)
- Code duplication identification
- Dead code detection
- Unused dependencies and imports
- Naming convention consistency
- Documentation coverage analysis

### Architecture Review
- Design pattern identification and improvements
- Separation of concerns evaluation
- Dependency injection opportunities
- SOLID principles compliance
- Clean architecture implementation
- Microservices decomposition possibilities

### Security Vulnerabilities
- Input validation and sanitization
- Authentication and authorization flaws
- Cryptographic implementation issues
- Dependency security vulnerabilities
- Information disclosure risks
- Configuration security problems

### Performance Bottlenecks
- Algorithm efficiency analysis
- Database query optimization opportunities
- Memory usage optimization
- Caching strategy improvements
- Async/await pattern adoption
- Resource management optimization

## Refactoring Strategies

### Structural Refactoring
- Extract Method for long functions
- Extract Class for single responsibility
- Move Method to appropriate classes
- Replace Conditional with Polymorphism
- Replace Magic Numbers with Named Constants
- Introduce Parameter Object for long parameter lists

### Pattern Implementation
- Strategy Pattern for algorithm variations
- Factory Pattern for object creation
- Observer Pattern for event handling
- Command Pattern for operation encapsulation
- Decorator Pattern for feature extension
- Repository Pattern for data access

### Modern Language Features
- **Python**: Type hints, dataclasses, context managers, f-strings
- **JavaScript**: ES6+ features, async/await, destructuring, modules
- **Java**: Streams, Optional, var keyword, record classes
- **C#**: LINQ, async/await, nullable reference types, pattern matching

### Framework Modernization
- Migration to modern framework versions
- Adoption of current best practices
- Integration of modern development tools
- Implementation of current security standards
- Performance optimization techniques
- Testing framework upgrades

## Refactoring Plan

### Phase 1: Analysis and Planning
1. **Code Analysis**
   - Static code analysis with appropriate tools
   - Dependency analysis and mapping
   - Performance profiling and bottleneck identification
   - Security vulnerability assessment

2. **Impact Assessment**
   - Risk analysis for proposed changes
   - Testing strategy development
   - Rollback plan creation
   - Team communication plan

### Phase 2: Preparatory Changes
1. **Infrastructure Setup**
   - Test suite enhancement
   - CI/CD pipeline updates
   - Code coverage measurement
   - Performance baseline establishment

2. **Safety Measures**
   - Feature flag implementation
   - Monitoring and alerting setup
   - Backup and recovery procedures
   - Gradual rollout strategy

### Phase 3: Implementation
1. **Incremental Refactoring**
   - Small, isolated changes
   - Continuous testing and validation
   - Regular code review cycles
   - Performance monitoring

2. **Pattern Implementation**
   - Design pattern introduction
   - Architecture improvement
   - Modern feature adoption
   - Code organization enhancement

### Phase 4: Validation and Optimization
1. **Quality Assurance**
   - Comprehensive testing
   - Performance validation
   - Security verification
   - Code review completion

2. **Documentation Update**
   - Architecture documentation
   - API documentation updates
   - Developer guide revisions
   - Deployment procedure updates

## Testing Strategy
- Maintain existing functionality through regression tests
- Add unit tests for refactored components
- Implement integration tests for modified interfaces
- Performance tests for optimized code
- Security tests for vulnerability fixes
- User acceptance testing for UI changes

## Risk Mitigation
- Gradual refactoring approach
- Comprehensive test coverage
- Code review requirements
- Rollback procedures
- Feature flags for new implementations
- Monitoring and alerting for early issue detection

## Success Metrics
- Code complexity reduction (cyclomatic complexity)
- Test coverage improvement
- Performance metrics enhancement
- Security vulnerability reduction
- Development velocity improvement
- Maintenance cost reduction

## Deliverables
1. **Refactored Code**
   - Modernized codebase with improved patterns
   - Enhanced performance and security
   - Improved maintainability and readability
   - Updated documentation and comments

2. **Analysis Reports**
   - Before/after comparison analysis
   - Performance improvement metrics
   - Security vulnerability fixes
   - Code quality improvements

3. **Documentation Updates**
   - Architecture documentation
   - API documentation
   - Developer guidelines
   - Deployment procedures

4. **Testing Suite**
   - Enhanced test coverage
   - Performance benchmarks
   - Security validation tests
   - Regression test suite

## Migration Guide
- Step-by-step refactoring process
- Breaking changes documentation
- Team training materials
- Best practices guidelines
- Troubleshooting procedures
- Performance optimization tips

Reference the following instruction files:
- [General Coding Guidelines](../instructions/general-coding.instructions.md)
- [Language-specific Guidelines](../instructions/)
- [Security Review Guidelines](../instructions/code-review.instructions.md)

Generate a comprehensive refactoring plan with incremental improvements and risk mitigation strategies.
