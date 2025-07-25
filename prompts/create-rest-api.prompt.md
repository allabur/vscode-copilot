---
mode: "agent"
tools: ["vscode"]
description: "Create a complete REST API with CRUD operations"
---

# Create REST API

Generate a complete REST API with CRUD operations for the specified resource.

## API Specifications
- **Resource**: ${input:resourceName:Enter resource name (e.g., users, products, orders)}
- **Framework**: ${input:framework:Choose framework (express, fastapi, spring-boot, asp.net)}
- **Database**: ${input:database:Choose database (postgresql, mongodb, mysql, sqlite)}

## API Requirements

### Endpoints Structure
```
GET    /api/${input:resourceName}/        - List all resources (with filtering, pagination)
GET    /api/${input:resourceName}/:id     - Get single resource by ID
POST   /api/${input:resourceName}/        - Create new resource
PUT    /api/${input:resourceName}/:id     - Update existing resource (full update)
PATCH  /api/${input:resourceName}/:id     - Update existing resource (partial update)
DELETE /api/${input:resourceName}/:id     - Delete resource by ID
```

### Additional Endpoints (if applicable)
- `GET /api/${input:resourceName}/search` - Advanced search functionality
- `GET /api/${input:resourceName}/export` - Export data in various formats
- `POST /api/${input:resourceName}/bulk` - Bulk operations

## Technical Requirements

### Request/Response Format
- Use JSON for all API communications
- Implement proper HTTP status codes
- Include pagination metadata for list endpoints
- Use consistent error response format
- Include API versioning in URL or headers

### Data Validation
- Validate all input data using appropriate schema validation
- Sanitize inputs to prevent injection attacks
- Implement field-level validation rules
- Return detailed validation error messages

### Security Features
- JWT authentication and authorization
- Rate limiting to prevent abuse
- Input sanitization and validation
- CORS configuration
- Security headers (helmet.js or similar)
- API key authentication for service-to-service calls

### Database Integration
- Use ORM/ODM for database operations
- Implement proper connection pooling
- Add database migrations
- Include database indexing for performance
- Implement soft deletes where appropriate

### Error Handling
- Centralized error handling middleware
- Proper logging of errors and requests
- Consistent error response format
- Graceful handling of database connection errors

## Performance & Scalability

### Caching Strategy
- Implement response caching for GET requests
- Use Redis or similar for session storage
- Cache frequently accessed data
- Implement cache invalidation strategies

### Monitoring & Logging
- Request/response logging
- Performance metrics collection
- Health check endpoints
- Error tracking and alerting

## Code Structure
```
src/
├── controllers/     # Request handlers
├── models/         # Data models/schemas
├── routes/         # Route definitions
├── middleware/     # Custom middleware
├── services/       # Business logic
├── validators/     # Input validation schemas
├── config/         # Configuration files
├── utils/          # Utility functions
└── tests/          # Test files
```

## Documentation
Generate the following documentation:
1. **OpenAPI/Swagger specification**
2. **API usage examples** for each endpoint
3. **Authentication guide**
4. **Error codes documentation**
5. **Rate limiting information**
6. **Database schema documentation**

## Testing Suite
Include comprehensive tests:
- **Unit tests** for individual functions
- **Integration tests** for API endpoints
- **Load tests** for performance validation
- **Security tests** for vulnerability assessment

## Environment Configuration
- Development, staging, and production configs
- Environment variable management
- Docker configuration for containerization
- CI/CD pipeline configuration

## Quality Assurance
- Code linting and formatting rules
- Pre-commit hooks
- Automated testing in CI pipeline
- Code coverage reporting
- Security vulnerability scanning

Reference the following instruction files:
- [General Coding Guidelines](../instructions/general-coding.instructions.md)
- [Security Review Guidelines](../instructions/code-review.instructions.md)
- [Test Generation Guidelines](../instructions/test-generation.instructions.md)

Generate a production-ready REST API following industry best practices.
