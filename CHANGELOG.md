# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.2.0] - 2026-04-15

### Added
- Initial Docker Compose configuration for production environment
- Production Docker Compose setup with service definitions and health checks
- Enhanced Docker management script with environment variable loading
- Nginx startup script with configuration templating
- Custom entrypoint script for web server startup with enhanced configuration

### Changed
- **BREAKING**: Upgraded LangChain packages to 1.0+ (langchain-core, langchain-community, langchain-openai, langchain-ollama, langchain-huggingface)
- **BREAKING**: Upgraded LangGraph from 0.6.x to 1.0.x
- **BREAKING**: Upgraded Pandas from 2.3.x to 3.0.x
- **BREAKING**: Upgraded FastAPI from 0.116.x to 0.135.x
- **BREAKING**: Upgraded Svelte packages to latest versions with Svelte 5 compatibility
- **BREAKING**: Upgraded various @langchain packages in frontend
- Updated Docker configuration to use pre-built images instead of build context
- Refactored code structure for improved readability and maintainability
- Enhanced vector store loading logic with better error handling
- Updated API service configuration in docker-compose
- Upgraded GitHub Actions (checkout 4→5→6, setup-node 4→5→6, docker actions to v4+)
- Improved agent variable naming and JSON references

### Dependencies - Backend
- Upgraded alembic from 1.16.4 to 1.18.4
- Upgraded apscheduler from 3.11.0 to 3.11.2
- Upgraded arxiv from 2.2.0 to 2.4.1
- Upgraded aiohttp from 3.12.15 to 3.13.4
- Upgraded beautifulsoup4 from 4.13.4 to 4.14.3
- Upgraded feedparser from 6.0.11 to 6.0.12
- Upgraded ipykernel from 6.30.1 to 7.2.0
- Upgraded ipython from 9.4.0 to 9.12.0
- Upgraded ipywidgets from 8.1.7 to 8.1.8
- Upgraded langchain from 0.3.27 to 1.0.3
- Upgraded langchain-text-splitters from 0.3.9 to 1.0.0
- Upgraded langchain-qdrant from 0.2.0 to 0.2.1
- Upgraded langchain-together from 0.3.1 to 0.4.0
- Upgraded langchain-experimental from 0.3.4 to 0.4.1
- Upgraded matplotlib from 3.10.5 to 3.10.8
- Upgraded psutil from 7.0.0 to 7.2.2
- Upgraded psycopg2-binary from 2.9.10 to 2.9.11
- Upgraded pydantic from 2.11.7 to 2.12.5
- Upgraded pytest from 8.4.1 to 9.0.2
- Upgraded pytest-asyncio from 1.1.0 to 1.3.0
- Upgraded pytest-cov from 6.2.1 to 7.1.0
- Upgraded pytest-mock from 3.14.1 to 3.15.1
- Upgraded python-dotenv from 1.1.1 to 1.2.2
- Upgraded qdrant-client from 1.15.1 to 1.17.1
- Upgraded ragas from 0.3.0 to 0.4.3
- Upgraded sqlalchemy from 2.0.42 to 2.0.48
- Upgraded tqdm from 4.67.1 to 4.67.3
- Upgraded uvicorn from 0.35.0 to 0.42.0
- Upgraded websockets from 15.0.1 to 16.0

### Dependencies - Frontend
- Upgraded Svelte packages with Svelte 5 compatibility updates
- Upgraded @langchain/langgraph from 0.4.4 to 1.0.15
- Upgraded @langchain/langgraph-sdk from 0.0.107 to 1.8.0
- Upgraded bits-ui from 2.9.1 to 2.16.3
- Upgraded lucide-svelte from 0.536.0 to 0.575.0
- Upgraded @lucide/svelte to 1.0.1
- Upgraded marked from 16.4.2 to 17.0.5
- Upgraded prettier from 3.7.3 to 3.8.1
- Upgraded prettier-plugin-svelte to 3.5.1
- Upgraded shadcn-svelte from 1.0.12 to 1.1.1
- Upgraded tailwindcss from 4.1.17 to 4.2.2
- Upgraded @tailwindcss/forms to 0.5.11
- Upgraded @tailwindcss/vite to 4.2.2
- Upgraded tailwind-merge from 3.4.0 to 3.5.0
- Upgraded tailwind-variants from 2.1.0 to 3.2.2
- Upgraded vite from 7.0.6 to 7.3.1
- Upgraded vite-plugin-devtools-json to 1.0.0
- Upgraded @internationalized/date to 3.12.0
- Upgraded acorn from 8.15.0 to 8.16.0
- Upgraded @sveltejs/kit and @sveltejs/vite-plugin-svelte to latest

### Fixed
- Fixed typo in agent variable name and corresponding JSON reference
- Improved error handling in vector store loading
- Enhanced code structure and readability
- Corrected API service configuration references

### Security
- Updated Docker actions to version 4.0+ for improved security
- Enhanced dependencies to latest versions with security patches

## [0.1.5] - 2025-08-09

### Added
- Comprehensive entrypoint system with standalone startup script
- First-time execution detection and setup process
- Database existence check and creation logic
- Timezone and user agent configuration to environment setup
- Default job scheduling with environment configuration
- Comprehensive database migration system using Alembic
- System health monitoring and detailed startup banners
- API access control with nginx proxy and dynamic key loading
- CORS support for LangGraph API
- Incremental fallback threshold for document processing
- Comprehensive test suites for various components
- Semantic chunking configuration and implementation
- ChunkingStrategy enum implementation
- Enhanced API documentation with detailed descriptions
- Pipeline scheduling functionality
- Modular architecture with improved import paths
- Custom exceptions and utility tools
- Performance monitoring and optimization services
- Vector store management capabilities
- Backup management functionality
- Health checker functionality
- Enhanced startup process with detailed banners and system information display
- Database migration system with comprehensive error handling
- Default job scheduling functionality
- Comprehensive test coverage for core components

### Changed
- **BREAKING**: Renamed `py-src` folder to `backend` for better organization
- **BREAKING**: Updated import paths and configuration to reflect backend directory structure
- Migrated from legacy test files to pytest framework
- Refactored pipeline engine and job functions
- Enhanced embedding initialization
- Improved scheduler initialization error handling
- Updated document loading URL handling and vector store loading logic
- Enhanced pipeline configuration and logging
- Improved migration status checking logic
- Consolidated startup logic into a single system
- Updated LangGraph agent configuration for improved functionality
- Refactored codebase to modular architecture
- Enhanced scheduler API to include job execution args and kwargs
- Increased max workers and updated misfire grace time
- Improved document processing pipeline with better error handling
- Improved startup logic consolidation
- Enhanced pipeline configuration and logging
- Updated LangGraph configuration for better agent functionality

### Removed
- Legacy parameters from pipeline execution
- Deprecated job_functions module
- Chainlit dependencies for improved maintainability
- Outdated blog posts and related tools
- Legacy test files (converted to pytest)
- Demo pipeline functionality

### Fixed
- Timezone-aware datetime usage across multiple files
- Database URL sanitization for enhanced security
- Scheduler initialization error handling
- Document loader URL handling
- Job configuration access method compatibility
- Frontend build errors and Svelte 5 deprecation issues
- Input component binding for Svelte 5
- TypeScript errors in frontend components
- Dark mode text visibility issues
- System settings management reactivity
- Database creation logic for multiple databases
- Migration status checking accuracy
- Startup logging and entrypoint messages clarity

### Security
- Enhanced database URL sanitization to prevent sensitive information exposure
- Implemented API access control with nginx proxy
- Added CORS support with proper configuration
- Improved security schemes in OpenAPI schema

## [v2025.05.16-docs14] - 2025-05-16

### Added
- Enhanced documentation system
- Improved API documentation structure

## [v2025.05.15-docs14] - 2025-05-15

### Added
- Documentation versioning system
- Comprehensive API documentation

## [0.1.1] - 2025-06-01

### Added
- Initial release of Let's Talk interactive AI chat system
- Core RAG (Retrieval-Augmented Generation) functionality
- Support for multiple embedding models
- Qdrant vector database integration
- LangChain and LangGraph orchestration
- Document ingestion from file system and websites
- Advanced text processing with recursive splitting and semantic chunking
- Multiple retriever support (BM25, multiple query retrievers, semantic search)
- GPT-4o-mini and GPT-4.1 language model support
- Custom Svelte frontend component
- Docker containerization support
- Basic API endpoints for chat functionality

### Technical Features
- **Embedding Models**: Snowflake Arctic Embed L v2.0 support
- **Vector Database**: Qdrant for efficient content indexing
- **Language Models**: OpenAI GPT models with configurable providers
- **Frontend**: Svelte-based chat interface
- **Backend**: FastAPI with comprehensive endpoint support
- **Deployment**: Docker and docker-compose configuration

### Documentation
- Comprehensive README with setup instructions
- Environment configuration examples
- Feature descriptions and technical implementation details

---

## Migration Notes

### From 0.1.1 to 0.1.5+

1. **Directory Structure Change**: The `py-src` directory has been renamed to `backend`. Update any scripts or configurations that reference the old path.

2. **Import Path Updates**: All Python import paths have been updated to reflect the new `backend` directory structure.

3. **Database Migration**: A new Alembic-based database migration system has been implemented. Run migrations using the provided migration scripts.

4. **Environment Variables**: New environment variables have been added for timezone, user agent, and database configuration. Update your `.env` file accordingly.

5. **Testing Framework**: Tests have been migrated to pytest. Use `uv run pytest` instead of the previous test commands.

6. **Startup Process**: A new entrypoint system has been implemented. Use the provided startup scripts for development and production.

## Development Guidelines

- Always use `uv` for Python package management
- Use `pnpm` for JavaScript/TypeScript dependencies  
- Follow the new modular architecture when making changes
- Run tests with `uv run pytest` before submitting changes
- Use the provided development scripts for consistent startup processes

## Contributors

- Muhammad Afzaal (@mafzaal)
- Dependabot for automated dependency updates
- Copilot SWE Agent for various feature implementations and bug fixes
