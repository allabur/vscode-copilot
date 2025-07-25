---
mode: "agent"
tools: ["vscode", "terminal"]
description: "Generate comprehensive unit tests for existing code"
---

# Generate Unit Tests

Create comprehensive unit tests for the specified code components.

## Target Code
Please specify the files or functions you want to test:
${input:targetFiles:Enter file paths or function names to test}

## Test Framework Setup
Automatically detect and use the appropriate testing framework:
- **Python**: pytest, unittest
- **JavaScript/TypeScript**: Jest, Vitest, Mocha
- **Java**: JUnit
- **C#**: NUnit, xUnit

## Test Generation Requirements

### Test Coverage Goals
- Achieve minimum 80% code coverage
- Test all public methods and functions
- Include edge cases and error scenarios
- Test both positive and negative paths
- Cover all conditional branches

### Test Categories
1. **Unit Tests**: Test individual functions/methods in isolation
2. **Integration Tests**: Test component interactions
3. **Property-Based Tests**: Test with random inputs (when applicable)
4. **Performance Tests**: Basic performance benchmarks for critical paths

### Test Structure
Each test should follow the AAA pattern:
- **Arrange**: Set up test data and mocks
- **Act**: Execute the code under test
- **Assert**: Verify the expected behavior

### Mock Strategy
- Mock external dependencies (APIs, databases, file system)
- Use dependency injection for better testability
- Create realistic mock data
- Verify mock interactions when relevant

## Specific Test Scenarios

### Happy Path Tests
- Test normal operation with valid inputs
- Verify expected outputs and side effects
- Test successful API calls and database operations

### Edge Case Tests
- Empty inputs, null values, undefined
- Boundary values (min/max, empty arrays)
- Large datasets and stress conditions
- Concurrent access scenarios

### Error Handling Tests
- Invalid inputs and malformed data
- Network failures and timeouts
- Database connection errors
- Permission and authorization failures
- Resource exhaustion scenarios

### State Management Tests
- Initial state validation
- State transitions and mutations
- State persistence and recovery
- Concurrent state modifications

## Test File Organization
```
├── tests/
│   ├── unit/
│   │   ├── components/
│   │   ├── services/
│   │   └── utils/
│   ├── integration/
│   ├── fixtures/
│   └── helpers/
```

## Test Naming Convention
- Use descriptive test names that explain the scenario
- Format: `test_function_name_when_condition_then_expected_result`
- Group related tests using describe/context blocks

## Quality Standards
- Each test should be independent and isolated
- Tests should be deterministic and repeatable
- Use appropriate assertions that provide clear failure messages
- Include setup and teardown when needed
- Add comments for complex test scenarios

## Deliverables
Generate the following for each target component:
1. **Test file** with comprehensive test suite
2. **Test data fixtures** for complex scenarios
3. **Mock utilities** for external dependencies
4. **Test configuration** files if needed
5. **Documentation** explaining test approach and coverage

## Coverage Report
After generating tests, provide:
- Coverage percentage by component
- List of uncovered code paths
- Recommendations for additional test scenarios
- Performance benchmarks for critical functions

Reference the [Test Generation Guidelines](../instructions/test-generation.instructions.md) for detailed best practices.
