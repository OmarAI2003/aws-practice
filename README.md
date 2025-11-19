# AWS Bedrock Practice Project

A hands-on project demonstrating AWS Bedrock integration with Knowledge Bases, Guardrails, and Python applications.

## Project Structure

### AI Project - Bedrock & Python Solution
- **Streamlit Chat App** (`app.py`) - Interactive chat interface with Bedrock LLM integration
- **Bedrock Utils** (`bedrock_utils.py`) - Core functions for model invocation, knowledge base queries, and prompt validation
- **Infrastructure** - Terraform modules for AWS resources:
  - Stack 1: VPC, Aurora Serverless PostgreSQL, S3 bucket
  - Stack 2: Bedrock Knowledge Base with vector storage
- **Sample Data** - Heavy machinery specification sheets (PDF format)

### Key Features
- **LLM Integration** - Claude 3 Haiku/Sonnet models via Bedrock Runtime
- **Knowledge Base** - RAG implementation with Aurora PostgreSQL vector storage
- **Prompt Validation** - Content filtering for heavy machinery domain
- **Infrastructure as Code** - Complete Terraform deployment

### Tech Stack
- **Frontend**: Streamlit
- **Backend**: Python, Boto3
- **Database**: Aurora Serverless PostgreSQL with pgvector
- **Storage**: S3 for document ingestion
- **Infrastructure**: Terraform, AWS Bedrock, VPC

## Quick Start
1. Deploy infrastructure: `terraform apply` in stack1/, then stack2/
2. Run SQL setup: Execute `scripts/aurora_sql.sql`
3. Upload documents: `python scripts/upload_s3.py`
4. Launch app: `streamlit run app.py`

## Requirements
- AWS CLI configured
- Terraform >= 0.12
- Python 3.10+
- Bedrock model access enabled