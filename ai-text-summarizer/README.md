# AI-Powered Text Summarizer Web App

## Overview
An intelligent web application that transforms lengthy text content into concise, meaningful summaries using advanced AI models. The system supports multiple summarization techniques including extractive, abstractive, and hybrid approaches with customizable summary lengths and styles.

## Use Case
**Target Users**: Content creators, researchers, students, professionals, journalists, business analysts
**Primary Function**: Convert long-form text content into digestible summaries while preserving key information and context

## Problem Solved
- **Information Overload**: Difficulty processing large volumes of text content
- **Time Constraints**: Limited time to read lengthy documents, articles, and reports
- **Content Curation**: Need to quickly identify key points from multiple sources
- **Research Efficiency**: Streamline literature review and content analysis processes
- **Accessibility**: Make complex content more accessible to diverse audiences

## Solution Architecture
The system leverages state-of-the-art language models with advanced prompt engineering to generate high-quality summaries. It supports multiple input formats, customizable summary parameters, and provides both API and web interfaces for seamless integration.

## Learning Outcomes
- **LLM Integration**: Work with multiple language models (OpenAI, Anthropic, Ollama)
- **Prompt Engineering**: Design effective prompts for different summarization tasks
- **Text Processing**: Implement chunking, preprocessing, and post-processing pipelines
- **API Development**: Build robust REST APIs with FastAPI
- **Frontend Development**: Create responsive React interfaces
- **Caching Strategies**: Implement intelligent caching for performance optimization

## Enterprise-Grade Tech Stack

### Backend Framework
- **FastAPI**: High-performance async web framework for Python
- **Pydantic**: Data validation and settings management
- **SQLAlchemy**: ORM for database operations
- **Alembic**: Database migration tool
- **Celery**: Distributed task queue for background processing

### AI/ML Stack
- **LangChain**: Framework for building LLM applications
- **OpenAI GPT-4**: Primary language model for summarization
- **Anthropic Claude**: Alternative LLM for enhanced reasoning
- **Ollama**: Local LLM deployment for privacy-sensitive use cases
- **Hugging Face Transformers**: Open-source summarization models
- **spaCy**: Natural language processing and text analysis
- **NLTK**: Text preprocessing and linguistic analysis
- **Sentence Transformers**: Text embeddings for similarity analysis

### Text Processing
- **PyPDF2**: PDF document processing
- **python-docx**: Microsoft Word document processing
- **BeautifulSoup4**: HTML content extraction
- **python-readability**: Content extraction from web pages
- **textstat**: Text readability and complexity analysis
- **langdetect**: Language detection for multilingual support

### Database & Storage
- **PostgreSQL**: Primary relational database
- **Redis**: Caching and session management
- **MongoDB**: Document storage for text content and summaries
- **MinIO**: S3-compatible object storage for file uploads

### Frontend
- **Next.js 14**: React framework with App Router
- **TypeScript**: Type-safe JavaScript development
- **Tailwind CSS**: Utility-first CSS framework
- **Shadcn/ui**: Modern UI component library
- **React Query**: Data fetching and state management
- **React Hook Form**: Form handling and validation
- **Monaco Editor**: Code editor for text input
- **React Markdown**: Markdown rendering

### DevOps & Infrastructure
- **Docker**: Containerization
- **Kubernetes**: Container orchestration
- **Helm**: Kubernetes package manager
- **Nginx**: Reverse proxy and load balancer
- **Prometheus**: Monitoring and alerting
- **Grafana**: Metrics visualization
- **ELK Stack**: Logging (Elasticsearch, Logstash, Kibana)

### Security & Authentication
- **Keycloak**: Identity and access management
- **OAuth 2.0/OIDC**: Authentication protocols
- **JWT**: Secure token-based authentication
- **bcrypt**: Password hashing
- **Rate Limiting**: API protection

### Testing & Quality
- **pytest**: Python testing framework
- **Jest**: JavaScript testing framework
- **Playwright**: End-to-end testing
- **Coverage.py**: Code coverage analysis
- **Black**: Python code formatting
- **ESLint**: JavaScript/TypeScript linting

## Project Structure
```
ai-text-summarizer/
├── backend/
│   ├── app/
│   │   ├── api/
│   │   │   ├── v1/
│   │   │   │   ├── endpoints/
│   │   │   │   │   ├── summarize.py
│   │   │   │   │   ├── documents.py
│   │   │   │   │   ├── history.py
│   │   │   │   │   ├── analytics.py
│   │   │   │   │   └── health.py
│   │   │   │   └── api.py
│   │   │   └── deps.py
│   │   ├── core/
│   │   │   ├── config.py
│   │   │   ├── security.py
│   │   │   └── database.py
│   │   ├── models/
│   │   │   ├── summary.py
│   │   │   ├── document.py
│   │   │   ├── user.py
│   │   │   └── analytics.py
│   │   ├── services/
│   │   │   ├── summarizer.py
│   │   │   ├── text_processor.py
│   │   │   ├── document_parser.py
│   │   │   ├── llm_service.py
│   │   │   └── cache_service.py
│   │   ├── summarizers/
│   │   │   ├── openai_summarizer.py
│   │   │   ├── claude_summarizer.py
│   │   │   ├── ollama_summarizer.py
│   │   │   ├── huggingface_summarizer.py
│   │   │   └── hybrid_summarizer.py
│   │   ├── schemas/
│   │   │   ├── summary.py
│   │   │   ├── document.py
│   │   │   └── analytics.py
│   │   ├── utils/
│   │   │   ├── text_utils.py
│   │   │   ├── chunking.py
│   │   │   ├── validation.py
│   │   │   └── metrics.py
│   │   └── main.py
│   ├── workers/
│   │   ├── summary_worker.py
│   │   ├── document_processor.py
│   │   └── analytics_worker.py
│   ├── tests/
│   ├── alembic/
│   ├── requirements.txt
│   └── Dockerfile
├── frontend/
│   ├── src/
│   │   ├── app/
│   │   │   ├── dashboard/
│   │   │   ├── summarize/
│   │   │   ├── history/
│   │   │   ├── analytics/
│   │   │   └── layout.tsx
│   │   ├── components/
│   │   │   ├── ui/
│   │   │   ├── summarizer/
│   │   │   ├── document/
│   │   │   ├── history/
│   │   │   └── analytics/
│   │   ├── lib/
│   │   │   ├── api.ts
│   │   │   ├── utils.ts
│   │   │   └── constants.ts
│   │   ├── hooks/
│   │   │   ├── useSummarizer.ts
│   │   │   ├── useHistory.ts
│   │   │   └── useAnalytics.ts
│   │   └── types/
│   ├── public/
│   ├── package.json
│   └── Dockerfile
├── k8s/
│   ├── backend/
│   ├── frontend/
│   ├── database/
│   └── ingress/
├── docker-compose.yml
├── docker-compose.prod.yml
└── README.md
```

## Getting Started

### Prerequisites
- Python 3.11+
- Node.js 18+
- Docker & Docker Compose
- PostgreSQL 15+
- Redis 7+

### Environment Setup
1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd ai-text-summarizer
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
   ```

4. **Environment Configuration**
   ```bash
   cp .env.example .env
   # Configure your environment variables
   ```

### Configuration

#### Environment Variables
```env
# Database
DATABASE_URL=postgresql://user:password@localhost:5432/summarizer_db
REDIS_URL=redis://localhost:6379
MONGODB_URL=mongodb://localhost:27017/text_summaries

# AI Services
OPENAI_API_KEY=your_openai_api_key
ANTHROPIC_API_KEY=your_anthropic_api_key
HUGGINGFACE_API_KEY=your_huggingface_key
OLLAMA_BASE_URL=http://localhost:11434

# Authentication
KEYCLOAK_URL=http://localhost:8080
KEYCLOAK_REALM=summarizer-platform
KEYCLOAK_CLIENT_ID=summarizer-client
KEYCLOAK_CLIENT_SECRET=your_client_secret

# Security
SECRET_KEY=your_secret_key
JWT_ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30

# Storage
MINIO_ENDPOINT=localhost:9000
MINIO_ACCESS_KEY=minioadmin
MINIO_SECRET_KEY=minioadmin
MINIO_BUCKET=text-documents

# Summarization Settings
DEFAULT_SUMMARY_LENGTH=medium
MAX_TEXT_LENGTH=50000
CHUNK_SIZE=4000
CHUNK_OVERLAP=200
SUPPORTED_LANGUAGES=en,es,fr,de,it,pt,ru,zh,ja,ko

# Rate Limiting
RATE_LIMIT_REQUESTS_PER_MINUTE=30
RATE_LIMIT_CHARACTERS_PER_HOUR=100000

# Cache Settings
CACHE_TTL_SECONDS=3600
ENABLE_SUMMARY_CACHE=true
```

### Running the Application

#### Development Mode
```bash
# Start infrastructure services
docker-compose up -d postgres redis mongodb minio keycloak

# Start backend
cd backend
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

# Start Celery workers
celery -A app.workers worker --loglevel=info

# Start frontend
cd frontend
npm run dev
```

#### Production Mode
```bash
docker-compose -f docker-compose.prod.yml up -d
```

#### Kubernetes Deployment
```bash
# Apply Kubernetes manifests
kubectl apply -f k8s/

# Install with Helm
helm install text-summarizer ./helm-chart
```

## API Endpoints

### Text Summarization
- `POST /api/v1/summarize/text` - Summarize plain text
- `POST /api/v1/summarize/url` - Summarize content from URL
- `POST /api/v1/summarize/document` - Summarize uploaded document
- `GET /api/v1/summarize/{summary_id}` - Get summary by ID
- `POST /api/v1/summarize/batch` - Batch summarization

### Document Management
- `POST /api/v1/documents/upload` - Upload document for summarization
- `GET /api/v1/documents/` - List uploaded documents
- `GET /api/v1/documents/{id}` - Get document details
- `DELETE /api/v1/documents/{id}` - Delete document

### Summary History
- `GET /api/v1/history/summaries` - Get user's summary history
- `GET /api/v1/history/summaries/{id}` - Get specific summary
- `PUT /api/v1/history/summaries/{id}` - Update summary metadata
- `DELETE /api/v1/history/summaries/{id}` - Delete summary
- `POST /api/v1/history/summaries/{id}/favorite` - Mark as favorite

### Analytics & Insights
- `GET /api/v1/analytics/usage` - Get usage statistics
- `GET /api/v1/analytics/performance` - Get performance metrics
- `GET /api/v1/analytics/popular-topics` - Get trending topics
- `GET /api/v1/analytics/user-stats` - Get user statistics

### Configuration
- `GET /api/v1/config/models` - List available models
- `GET /api/v1/config/languages` - List supported languages
- `POST /api/v1/config/preferences` - Update user preferences
- `GET /api/v1/config/limits` - Get usage limits

## Testing

### Backend Testing
```bash
cd backend
pytest tests/ -v --cov=app --cov-report=html
```

### Frontend Testing
```bash
cd frontend
npm run test
npm run test:e2e
```

### Summarization Quality Testing
```bash
# Test different summarization models
python scripts/test_summarizers.py

# Evaluate summary quality
python scripts/evaluate_summaries.py
```

## Performance Optimization

### Response Time Targets
- Text summarization: < 10 seconds
- Document processing: < 30 seconds
- URL content extraction: < 15 seconds
- Cached summaries: < 1 second

### Scalability Features
- Horizontal scaling with Kubernetes
- Redis caching for repeated content
- Async processing with Celery
- CDN for static assets
- Database connection pooling

## Security Measures

### Data Protection
- Input sanitization and validation
- Secure file upload handling
- Content encryption at rest
- GDPR compliance for user data

### Access Control
- JWT-based authentication
- Rate limiting per user/IP
- API key management
- Input size limitations

## Deployment

### Docker Deployment
```bash
# Build images
docker-compose build

# Deploy to production
docker-compose -f docker-compose.prod.yml up -d
```

### Kubernetes Deployment
```bash
# Create namespace
kubectl create namespace text-summarizer

# Deploy application
kubectl apply -f k8s/ -n text-summarizer

# Check deployment status
kubectl get pods -n text-summarizer
```

## Advanced Features

### Summarization Techniques
- **Extractive Summarization**: Select key sentences from original text
- **Abstractive Summarization**: Generate new sentences that capture meaning
- **Hybrid Approach**: Combine extractive and abstractive methods
- **Multi-Document Summarization**: Summarize multiple related documents
- **Query-Focused Summarization**: Generate summaries based on specific questions

### Customization Options
- **Summary Length**: Short, medium, long, or custom word count
- **Summary Style**: Bullet points, paragraph, executive summary
- **Focus Areas**: Technical, business, academic, general audience
- **Language Support**: Multi-language input and output
- **Tone Adjustment**: Formal, casual, technical, simplified

### Content Processing
- **Document Formats**: PDF, DOCX, TXT, HTML, Markdown
- **Web Content**: URL extraction with content cleaning
- **Batch Processing**: Multiple documents simultaneously
- **Real-time Processing**: Streaming summarization for large texts
- **Content Validation**: Quality checks and error handling

### Analytics & Insights
- **Usage Metrics**: Track summarization patterns and preferences
- **Quality Metrics**: ROUGE scores and user feedback analysis
- **Performance Monitoring**: Response times and error rates
- **Content Analysis**: Topic modeling and trend identification

## Integration Capabilities

### API Integration
- **REST API**: Full-featured REST endpoints
- **Webhook Support**: Real-time notifications
- **Batch API**: Bulk processing capabilities
- **GraphQL**: Flexible query interface

### Third-Party Integrations
- **Content Management Systems**: WordPress, Drupal integration
- **Document Platforms**: Google Docs, Microsoft Office 365
- **Research Tools**: Zotero, Mendeley integration
- **Business Tools**: Slack, Microsoft Teams notifications

## Contributing

### Development Guidelines
1. Follow PEP 8 for Python code
2. Use TypeScript for frontend development
3. Write comprehensive tests for summarization logic
4. Document API changes and new features
5. Follow conventional commit messages

### Adding New Summarization Models
1. Implement model interface in `summarizers/`
2. Add model configuration options
3. Create comprehensive test cases
4. Update documentation and examples

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Support

### Documentation
- [API Documentation](./docs/api.md)
- [Model Comparison](./docs/models.md)
- [Integration Guide](./docs/integrations.md)
- [Deployment Guide](./docs/deployment.md)
- [Troubleshooting](./docs/troubleshooting.md)

### Community
- GitHub Issues for bug reports
- Discussions for feature requests
- Discord community for real-time support
- Monthly community calls for feedback

### Enterprise Support
For enterprise deployments, custom models, and professional services, contact our support team.

---

**Note**: This text summarization platform is designed to handle various content types while maintaining high quality and performance standards. It provides both simple and advanced summarization capabilities suitable for individual users and enterprise deployments.