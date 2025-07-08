When performing a code review, respond in german.

Our team uses Jira for tracking items of work.

## Development Guidelines

### Python SDK Requirements
- Always use the latest stable Python SDK versions for all cloud providers and services
- Prioritize official SDKs over community libraries
- Document all SDK versions in requirements.txt or pyproject.toml
- Regular updates and security patches are mandatory

### Licensing Requirements
- Only use GitHub projects with MIT license
- Verify LICENSE file or repository license badge before integration
- Document all external dependencies with their licenses
- Avoid GPL, AGPL, or proprietary licenses

### Docker Compose Architecture
- All solutions must be built using Docker Compose
- Create separate services for different components (API, Database, Frontend, etc.)
- Implement health checks for all services
- Define volumes for persistent data
- Use environment variables for configuration
- Ensure services communicate via Docker networks
- Solutions must be startable with a single `docker-compose up` command

### Code Quality Standards
- Code must be production-ready
- All services must be independently scalable
- Configuration through environment variables
- Implement logging and monitoring integration
- Follow security best practices
- Include comprehensive documentation

### Required Deliverables
When generating solutions, always provide:
1. Complete Python code with current SDKs
2. requirements.txt/pyproject.toml with current versions
3. Dockerfile(s) for all services
4. docker-compose.yml with service definitions, health checks, environment variables, volumes, and network configuration
5. README.md with setup and usage instructions
6. License documentation for all dependencies

### Azure Development Rules
- @azure Rule - Use Azure Tools: When handling Azure requests, always use available Azure tools
- @azure Rule - Use Azure Code Gen Best Practices: Invoke azure_development-get_code_gen_best_practices when generating Azure code
- @azure Rule - Use Azure Deployment Best Practices: Invoke azure_development-get_deployment_best_practices when deploying to Azure
- @azure Rule - Use Azure Functions Best Practices: Invoke azure_development-get_azure_function_code_gen_best_practices for Azure Functions
- @azure Rule - Use Azure SWA Best Practices: Invoke azure_development-get_swa_best_practices for static web apps
