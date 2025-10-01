# Enterprise RAG Agent with Admin Console

## Overview
A comprehensive enterprise-grade Retrieval-Augmented Generation (RAG) system with role-based access control, admin console, and multi-tenant architecture. This platform enables organizations to ingest, manage, and query their knowledge base while maintaining strict access controls and providing detailed analytics and auditing capabilities.

## Use Case
**Target Users**: Enterprise organizations, knowledge managers, IT administrators, business analysts, employees
**Primary Function**: Centralized knowledge management with intelligent querying, role-based access, and comprehensive administration

## Problem Solved
- **Information Silos**: Fragmented knowledge across different departments and systems
- **Access Control**: Lack of granular permissions for sensitive information
- **Knowledge Discovery**: Difficulty finding relevant information across large datasets
- **Compliance Requirements**: Need for audit trails and data governance
- **Scalability Issues**: Managing knowledge access for large organizations

## Solution Architecture
The system combines advanced RAG capabilities with enterprise-grade security, multi-tenancy, role-based access control, and comprehensive administration tools to provide a scalable, secure, and intelligent knowledge management platform.

## Learning Outcomes
- **Full-Stack Architecture**: Complete enterprise application development
- **Authentication & Authorization**: Implement Keycloak integration and RBAC
- **RAG Implementation**: Advanced retrieval-augmented generation techniques
- **Query Auditing**: Comprehensive logging and monitoring
- **Admin Controls**: Administrative interfaces and management tools
- **Multi-Tenancy**: Scalable multi-organization architecture

## Enterprise-Grade Tech Stack

### Backend Framework
- **FastAPI**: High-performance async web framework for Python
- **Pydantic**: Data validation and settings management
- **SQLAlchemy**: ORM for database operations
- **Alembic**: Database migration tool
- **Celery**: Distributed task queue for background processing
- **Apache Airflow**: Workflow orchestration for data pipelines

### AI/ML Stack
- **LangChain**: Framework for building LLM applications
- **OpenAI GPT-4**: Primary language model for query processing
- **Anthropic Claude**: Alternative LLM for enhanced reasoning
- **Hugging Face Transformers**: Open-source embedding models
- **Sentence Transformers**: Specialized embedding models
- **spaCy**: Natural language processing
- **NLTK**: Text processing and analysis

### Vector Databases & Search
- **Weaviate**: Vector database with hybrid search
- **ChromaDB**: Open-source vector database
- **Elasticsearch**: Full-text search and analytics
- **Pinecone**: Managed vector database
- **FAISS**: Facebook AI Similarity Search
- **Qdrant**: High-performance vector search engine

### Document Processing
- **PyPDF2**: PDF document processing
- **python-docx**: Microsoft Word document processing
- **openpyxl**: Excel spreadsheet processing
- **python-pptx**: PowerPoint presentation processing
- **BeautifulSoup4**: HTML/XML parsing
- **Tesseract OCR**: Optical character recognition
- **Apache Tika**: Universal document parser

### Database & Storage
- **PostgreSQL**: Primary relational database with vector extensions
- **Redis**: Caching, session management, and real-time features
- **MongoDB**: Document storage for unstructured data
- **MinIO**: S3-compatible object storage
- **TimescaleDB**: Time-series data for analytics
- **Apache Kafka**: Event streaming platform

### Frontend
- **Next.js 14**: React framework with App Router
- **TypeScript**: Type-safe JavaScript development
- **Tailwind CSS**: Utility-first CSS framework
- **Shadcn/ui**: Modern UI component library
- **React Query**: Data fetching and state management
- **React Hook Form**: Form handling and validation
- **Recharts**: Data visualization and analytics
- **React Table**: Advanced table components

### Authentication & Authorization
- **Keycloak**: Identity and access management
- **OAuth 2.0/OIDC**: Authentication protocols
- **JWT**: Secure token-based authentication
- **RBAC**: Role-based access control
- **ABAC**: Attribute-based access control
- **SAML 2.0**: Enterprise SSO integration

### DevOps & Infrastructure
- **Docker**: Containerization
- **Kubernetes**: Container orchestration
- **Helm**: Kubernetes package manager
- **Nginx**: Reverse proxy and load balancer
- **Traefik**: Modern reverse proxy with automatic service discovery
- **Prometheus**: Monitoring and alerting
- **Grafana**: Metrics visualization and dashboards
- **ELK Stack**: Logging (Elasticsearch, Logstash, Kibana)
- **Jaeger**: Distributed tracing

### Security & Compliance
- **HashiCorp Vault**: Secrets management
- **OWASP ZAP**: Security testing
- **Falco**: Runtime security monitoring
- **Open Policy Agent (OPA)**: Policy-based access control
- **Cert-Manager**: Automatic TLS certificate management

### Testing & Quality
- **pytest**: Python testing framework
- **Jest**: JavaScript testing framework
- **Playwright**: End-to-end testing
- **Coverage.py**: Code coverage analysis
- **Black**: Python code formatting
- **ESLint**: JavaScript/TypeScript linting
- **SonarQube**: Code quality analysis

## Project Structure
```
role-based-rag-agent/
├── backend/
│   ├── app/
│   │   ├── api/
│   │   │   ├── v1/
│   │   │   │   ├── endpoints/
│   │   │   │   │   ├── auth.py
│   │   │   │   │   ├── documents.py
│   │   │   │   │   ├── queries.py
│   │   │   │   │   ├── admin.py
│   │   │   │   │   ├── analytics.py
│   │   │   │   │   ├── users.py
│   │   │   │   │   ├── roles.py
│   │   │   │   │   ├── tenants.py
│   │   │   │   │   └── integrations.py
│   │   │   │   └── api.py
│   │   │   └── deps.py
│   │   ├── core/
│   │   │   ├── config.py
│   │   │   ├── security.py
│   │   │   ├── database.py
│   │   │   ├── auth.py
│   │   │   └── permissions.py
│   │   ├── models/
│   │   │   ├── user.py
│   │   │   ├── tenant.py
│   │   │   ├── role.py
│   │   │   ├── document.py
│   │   │   ├── query.py
│   │   │   ├── audit.py
│   │   │   └── knowledge_base.py
│   │   ├── services/
│   │   │   ├── rag_service.py
│   │   │   ├── document_processor.py
│   │   │   ├── vector_store.py
│   │   │   ├── query_engine.py
│   │   │   ├── auth_service.py
│   │   │   ├── admin_service.py
│   │   │   ├── audit_service.py
│   │   │   └── analytics_service.py
│   │   ├── processors/
│   │   │   ├── pdf_processor.py
│   │   │   ├── docx_processor.py
│   │   │   ├── excel_processor.py
│   │   │   ├── pptx_processor.py
│   │   │   ├── html_processor.py
│   │   │   └── ocr_processor.py
│   │   ├── schemas/
│   │   │   ├── auth.py
│   │   │   ├── document.py
│   │   │   ├── query.py
│   │   │   ├── admin.py
│   │   │   └── analytics.py
│   │   ├── utils/
│   │   │   ├── embeddings.py
│   │   │   ├── chunking.py
│   │   │   ├── permissions.py
│   │   │   └── audit.py
│   │   └── main.py
│   ├── workers/
│   │   ├── document_ingestion.py
│   │   ├── embedding_generation.py
│   │   ├── index_maintenance.py
│   │   └── analytics_processing.py
│   ├── tests/
│   ├── alembic/
│   ├── requirements.txt
│   └── Dockerfile
├── frontend/
│   ├── src/
│   │   ├── app/
│   │   │   ├── (auth)/
│   │   │   │   ├── login/
│   │   │   │   └── callback/
│   │   │   ├── dashboard/
│   │   │   ├── knowledge-base/
│   │   │   ├── query/
│   │   │   ├── admin/
│   │   │   │   ├── users/
│   │   │   │   ├── roles/
│   │   │   │   ├── tenants/
│   │   │   │   ├── documents/
│   │   │   │   ├── analytics/
│   │   │   │   └── audit/
│   │   │   ├── analytics/
│   │   │   └── layout.tsx
│   │   ├── components/
│   │   │   ├── ui/
│   │   │   ├── auth/
│   │   │   ├── admin/
│   │   │   ├── query/
│   │   │   ├── documents/
│   │   │   ├── analytics/
│   │   │   └── layout/
│   │   ├── lib/
│   │   │   ├── auth.ts
│   │   │   ├── api.ts
│   │   │   ├── permissions.ts
│   │   │   └── utils.ts
│   │   ├── hooks/
│   │   │   ├── useAuth.ts
│   │   │   ├── usePermissions.ts
│   │   │   └── useAnalytics.ts
│   │   └── types/
│   ├── public/
│   ├── package.json
│   └── Dockerfile
├── admin-console/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Dashboard/
│   │   │   ├── UserManagement/
│   │   │   ├── RoleManagement/
│   │   │   ├── TenantManagement/
│   │   │   ├── DocumentManagement/
│   │   │   ├── Analytics/
│   │   │   └── AuditLogs/
│   │   ├── pages/
│   │   └── utils/
│   └── package.json
├── data-pipelines/
│   ├── airflow/
│   │   ├── dags/
│   │   │   ├── document_ingestion.py
│   │   │   ├── embedding_update.py
│   │   │   ├── index_optimization.py
│   │   │   └── analytics_processing.py
│   │   └── plugins/
│   └── scripts/
├── k8s/
│   ├── namespace.yaml
│   ├── backend/
│   ├── frontend/
│   ├── admin-console/
│   ├── databases/
│   ├── vector-stores/
│   ├── keycloak/
│   ├── monitoring/
│   └── ingress/
├── helm-chart/
│   ├── Chart.yaml
│   ├── values.yaml
│   └── templates/
├── docker-compose.yml
├── docker-compose.prod.yml
└── README.md
```

## Getting Started

### Prerequisites
- Python 3.11+
- Node.js 18+
- Docker & Docker Compose
- Kubernetes cluster (for production)
- PostgreSQL 15+
- Redis 7+
- Elasticsearch 8+

### Environment Setup
1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd role-based-rag-agent
   ```

2. **Backend Setup**
   ```bash
   cd backend
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Frontend Setup**
   ```bash
   cd frontend
   npm install
   
   cd ../admin-console
   npm install
   ```

4. **Environment Configuration**
   ```bash
   cp .env.example .env
   # Configure your environment variables
   ```

### Configuration

#### Environment Variables
```env
# Database Configuration
DATABASE_URL=postgresql://user:password@localhost:5432/rag_enterprise_db
REDIS_URL=redis://localhost:6379
MONGODB_URL=mongodb://localhost:27017/rag_documents
TIMESCALEDB_URL=postgresql://user:password@localhost:5432/rag_analytics

# Vector Databases
WEAVIATE_URL=http://localhost:8080
WEAVIATE_API_KEY=your_weaviate_key
CHROMADB_HOST=localhost
CHROMADB_PORT=8000
ELASTICSEARCH_URL=http://localhost:9200
ELASTICSEARCH_USERNAME=elastic
ELASTICSEARCH_PASSWORD=your_password
PINECONE_API_KEY=your_pinecone_key
PINECONE_ENVIRONMENT=your_environment

# AI Services
OPENAI_API_KEY=your_openai_api_key
ANTHROPIC_API_KEY=your_anthropic_api_key
HUGGINGFACE_API_KEY=your_huggingface_key

# Authentication & Authorization
KEYCLOAK_URL=http://localhost:8080
KEYCLOAK_REALM=rag-enterprise
KEYCLOAK_CLIENT_ID=rag-client
KEYCLOAK_CLIENT_SECRET=your_client_secret
KEYCLOAK_ADMIN_USERNAME=admin
KEYCLOAK_ADMIN_PASSWORD=admin_password

# Security
SECRET_KEY=your_secret_key
JWT_ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30
REFRESH_TOKEN_EXPIRE_DAYS=7

# Object Storage
MINIO_ENDPOINT=localhost:9000
MINIO_ACCESS_KEY=minioadmin
MINIO_SECRET_KEY=minioadmin
MINIO_BUCKET=rag-documents

# Message Queue
KAFKA_BOOTSTRAP_SERVERS=localhost:9092
CELERY_BROKER_URL=redis://localhost:6379/0
CELERY_RESULT_BACKEND=redis://localhost:6379/0

# Monitoring & Logging
PROMETHEUS_URL=http://localhost:9090
GRAFANA_URL=http://localhost:3000
ELASTICSEARCH_LOGS_INDEX=rag-logs
JAEGER_ENDPOINT=http://localhost:14268/api/traces

# Application Settings
MAX_DOCUMENT_SIZE=100MB
CHUNK_SIZE=1000
CHUNK_OVERLAP=200
MAX_QUERY_LENGTH=1000
EMBEDDING_MODEL=sentence-transformers/all-MiniLM-L6-v2
LLM_MODEL=gpt-4
VECTOR_DIMENSION=384

# Multi-tenancy
DEFAULT_TENANT=default
TENANT_ISOLATION_LEVEL=strict
MAX_TENANTS_PER_INSTANCE=100

# Rate Limiting
RATE_LIMIT_QUERIES_PER_MINUTE=60
RATE_LIMIT_DOCUMENTS_PER_HOUR=100
RATE_LIMIT_ADMIN_ACTIONS_PER_MINUTE=30
```

### Running the Application

#### Development Mode
```bash
# Start infrastructure services
docker-compose up -d postgres redis mongodb elasticsearch weaviate keycloak minio kafka

# Start backend
cd backend
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

# Start Celery workers
celery -A app.workers worker --loglevel=info

# Start frontend
cd frontend
npm run dev

# Start admin console
cd admin-console
npm run dev
```

#### Production Mode
```bash
# Deploy with Docker Compose
docker-compose -f docker-compose.prod.yml up -d

# Or deploy to Kubernetes
kubectl apply -f k8s/
```

#### Helm Deployment
```bash
# Install with Helm
helm repo add rag-enterprise ./helm-chart
helm install rag-platform rag-enterprise/rag-platform
```

## API Endpoints

### Authentication
- `POST /api/v1/auth/login` - User authentication
- `POST /api/v1/auth/logout` - User logout
- `POST /api/v1/auth/refresh` - Refresh access token
- `GET /api/v1/auth/me` - Get current user info
- `POST /api/v1/auth/change-password` - Change password

### Document Management
- `POST /api/v1/documents/upload` - Upload documents
- `GET /api/v1/documents/` - List documents with permissions
- `GET /api/v1/documents/{id}` - Get document details
- `PUT /api/v1/documents/{id}` - Update document metadata
- `DELETE /api/v1/documents/{id}` - Delete document
- `POST /api/v1/documents/{id}/reprocess` - Reprocess document

### Query & RAG
- `POST /api/v1/query/ask` - Submit query to RAG system
- `GET /api/v1/query/history` - Get query history
- `GET /api/v1/query/{id}` - Get query details
- `POST /api/v1/query/{id}/feedback` - Provide feedback on query result
- `GET /api/v1/query/suggestions` - Get query suggestions

### Knowledge Base
- `GET /api/v1/knowledge-base/collections` - List knowledge base collections
- `POST /api/v1/knowledge-base/collections` - Create collection
- `GET /api/v1/knowledge-base/collections/{id}` - Get collection details
- `PUT /api/v1/knowledge-base/collections/{id}` - Update collection
- `DELETE /api/v1/knowledge-base/collections/{id}` - Delete collection

### Admin - User Management
- `GET /api/v1/admin/users` - List all users
- `POST /api/v1/admin/users` - Create user
- `GET /api/v1/admin/users/{id}` - Get user details
- `PUT /api/v1/admin/users/{id}` - Update user
- `DELETE /api/v1/admin/users/{id}` - Delete user
- `POST /api/v1/admin/users/{id}/roles` - Assign roles to user

### Admin - Role Management
- `GET /api/v1/admin/roles` - List all roles
- `POST /api/v1/admin/roles` - Create role
- `GET /api/v1/admin/roles/{id}` - Get role details
- `PUT /api/v1/admin/roles/{id}` - Update role
- `DELETE /api/v1/admin/roles/{id}` - Delete role
- `POST /api/v1/admin/roles/{id}/permissions` - Assign permissions to role

### Admin - Tenant Management
- `GET /api/v1/admin/tenants` - List all tenants
- `POST /api/v1/admin/tenants` - Create tenant
- `GET /api/v1/admin/tenants/{id}` - Get tenant details
- `PUT /api/v1/admin/tenants/{id}` - Update tenant
- `DELETE /api/v1/admin/tenants/{id}` - Delete tenant

### Analytics & Reporting
- `GET /api/v1/analytics/usage` - Usage statistics
- `GET /api/v1/analytics/performance` - Performance metrics
- `GET /api/v1/analytics/user-activity` - User activity analytics
- `GET /api/v1/analytics/document-stats` - Document statistics
- `GET /api/v1/analytics/query-trends` - Query trend analysis

### Audit & Compliance
- `GET /api/v1/audit/logs` - Get audit logs
- `GET /api/v1/audit/user-actions` - User action history
- `GET /api/v1/audit/document-access` - Document access logs
- `GET /api/v1/audit/query-logs` - Query audit logs
- `POST /api/v1/audit/export` - Export audit data

## Testing

### Backend Testing
```bash
cd backend
pytest tests/ -v --cov=app --cov-report=html

# Test specific components
pytest tests/test_rag_service.py -v
pytest tests/test_auth.py -v
pytest tests/test_permissions.py -v
```

### Frontend Testing
```bash
cd frontend
npm run test
npm run test:e2e

cd ../admin-console
npm run test
```

### Integration Testing
```bash
# Test RAG pipeline
python scripts/test_rag_pipeline.py

# Test multi-tenancy
python scripts/test_multi_tenancy.py

# Test permissions
python scripts/test_rbac.py
```

## Performance Optimization

### Query Performance Targets
- Simple queries: < 2 seconds
- Complex queries: < 5 seconds
- Document ingestion: < 30 seconds per MB
- Embedding generation: < 10 seconds per document

### Scalability Features
- Horizontal scaling with Kubernetes
- Vector database sharding
- Distributed document processing
- Redis caching for frequent queries
- CDN for static assets
- Connection pooling and optimization

## Security & Compliance

### Data Protection
- End-to-end encryption for sensitive documents
- Field-level encryption for PII data
- Secure multi-tenant data isolation
- GDPR compliance with data retention policies
- SOC 2 Type II compliance ready

### Access Control
- Fine-grained role-based access control (RBAC)
- Attribute-based access control (ABAC)
- Document-level permissions
- Query result filtering based on permissions
- API rate limiting and throttling

### Audit & Compliance
- Comprehensive audit logging
- Query and access tracking
- Data lineage and provenance
- Compliance reporting
- Data retention and deletion policies

## Deployment

### Docker Deployment
```bash
# Build and deploy
docker-compose build
docker-compose -f docker-compose.prod.yml up -d

# Scale services
docker-compose up -d --scale backend=3 --scale worker=5
```

### Kubernetes Deployment
```bash
# Create namespace
kubectl create namespace rag-enterprise

# Deploy infrastructure
kubectl apply -f k8s/databases/ -n rag-enterprise
kubectl apply -f k8s/vector-stores/ -n rag-enterprise
kubectl apply -f k8s/keycloak/ -n rag-enterprise

# Deploy application
kubectl apply -f k8s/backend/ -n rag-enterprise
kubectl apply -f k8s/frontend/ -n rag-enterprise
kubectl apply -f k8s/admin-console/ -n rag-enterprise

# Setup ingress
kubectl apply -f k8s/ingress/ -n rag-enterprise
```

### Helm Deployment
```bash
# Install with custom values
helm install rag-platform ./helm-chart \
  --set global.domain=rag.company.com \
  --set keycloak.enabled=true \
  --set monitoring.enabled=true \
  --set autoscaling.enabled=true
```

## Advanced Features

### Multi-Tenancy
- **Tenant Isolation**: Complete data separation between organizations
- **Shared Resources**: Efficient resource utilization across tenants
- **Tenant-Specific Configuration**: Custom settings per organization
- **Billing Integration**: Usage tracking for billing purposes

### Advanced RAG Capabilities
- **Hybrid Search**: Combine vector and keyword search
- **Query Expansion**: Automatic query enhancement
- **Context Ranking**: Intelligent context selection
- **Multi-Modal RAG**: Support for images, tables, and charts
- **Conversational RAG**: Multi-turn conversation support

### Enterprise Integration
- **SSO Integration**: SAML, OIDC, LDAP support
- **API Gateway**: Centralized API management
- **Workflow Integration**: Connect with business processes
- **Data Connectors**: Integration with enterprise systems
- **Webhook Support**: Real-time event notifications

### Analytics & Intelligence
- **Usage Analytics**: Detailed usage patterns and trends
- **Performance Monitoring**: Real-time performance metrics
- **User Behavior Analysis**: Query patterns and preferences
- **Content Analytics**: Document usage and effectiveness
- **Predictive Analytics**: Forecast usage and capacity needs

## Admin Console Features

### Dashboard
- **System Overview**: Health, performance, and usage metrics
- **Real-Time Monitoring**: Live system status and alerts
- **Resource Utilization**: CPU, memory, storage usage
- **User Activity**: Active users and session information

### User Management
- **User Directory**: Complete user management interface
- **Role Assignment**: Assign and manage user roles
- **Permission Matrix**: Visual permission management
- **Bulk Operations**: Import/export users and bulk updates

### Content Management
- **Document Library**: Centralized document management
- **Collection Management**: Organize documents into collections
- **Metadata Management**: Custom metadata fields and schemas
- **Content Analytics**: Document usage and performance metrics

### System Administration
- **Configuration Management**: System-wide settings
- **Integration Management**: External system connections
- **Backup & Recovery**: Data backup and restoration tools
- **System Maintenance**: Scheduled maintenance and updates

## Contributing

### Development Guidelines
1. Follow PEP 8 for Python code
2. Use TypeScript for frontend development
3. Write comprehensive tests for all components
4. Document API changes and new features
5. Follow conventional commit messages
6. Ensure security best practices

### Architecture Guidelines
1. Maintain multi-tenant architecture principles
2. Implement proper error handling and logging
3. Follow microservices patterns where applicable
4. Ensure scalability and performance considerations
5. Maintain backward compatibility

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Support

### Documentation
- [Architecture Guide](./docs/architecture.md)
- [API Documentation](./docs/api.md)
- [Admin Guide](./docs/admin.md)
- [Deployment Guide](./docs/deployment.md)
- [Security Guide](./docs/security.md)
- [Troubleshooting](./docs/troubleshooting.md)

### Community
- GitHub Issues for bug reports
- Discussions for feature requests
- Slack workspace for community support
- Monthly community calls

### Enterprise Support
For enterprise deployments, custom integrations, professional services, and SLA-backed support, contact our enterprise team.

---

**Note**: This enterprise RAG platform is designed for production use with enterprise-grade security, scalability, and compliance features. It provides a comprehensive solution for organizational knowledge management with advanced AI capabilities.