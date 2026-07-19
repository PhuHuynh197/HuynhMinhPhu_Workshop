---
title: "Week 11 Worklog"
date: 2026-06-26
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives

* Implement the AI chatbot feature for the **PharmaCare AI** system using the RAG architecture.
* Prepare internal pharmacy knowledge documents for chatbot retrieval.
* Create Amazon S3 bucket to store knowledge documents.
* Configure Amazon Bedrock models for embedding generation and AI response generation.
* Create Amazon OpenSearch Serverless collection as the vector store.
* Configure VPC Endpoint, Security Group, and IAM Role for the AI Lambda functions.
* Create Lambda Indexing to process knowledge documents and store vectors in OpenSearch.
* Create Lambda Chatbot to receive user questions and return answers based on internal knowledge.
* Integrate chatbot API with API Gateway and frontend.

### Tasks to be carried out this week

| Day | Task | Start Date | Completion Date |
| --- | --- | --- | --- |
| 1 | - Started implementing the AI/RAG layer for **PharmaCare AI**. <br> - Reviewed the chatbot workflow in the system architecture. <br> - Prepared pharmacy knowledge documents in `.txt` format. <br> - Organized knowledge data into groups such as products, FAQ, medical guides, health articles, safety information, and indexes. | 26/06/2026 | 26/06/2026 |
| 2 | - Created Amazon S3 bucket `pharmacare-knowledge-docs-phu-2026`. <br> - Created the `knowledge/` prefix to store internal knowledge documents. <br> - Uploaded knowledge files to S3. <br> - Verified that the knowledge documents were ready for indexing. | 27/06/2026 | 27/06/2026 |
| 3 | - Configured Amazon Bedrock model access. <br> - Used `cohere.embed-multilingual-v3` to generate vector embeddings for Vietnamese and English knowledge content. <br> - Prepared Amazon Nova Micro as the LLM model for natural chatbot responses when LLM mode is enabled. <br> - Reviewed the embedding dimension and response generation workflow. | 28/06/2026 | 28/06/2026 |
| 4 | - Created Security Group for AI-related Lambda functions. <br> - Configured VPC Endpoint access for private AI workloads. <br> - Created S3 Gateway Endpoint so Lambda can read knowledge documents from S3. <br> - Created Bedrock Runtime VPC Endpoint so Lambda can call embedding and LLM models privately. <br> - Created OpenSearch Serverless VPC Endpoint so Lambda can access the vector store securely. | 29/06/2026 | 29/06/2026 |
| 5 | - Created Amazon OpenSearch Serverless collection named `pharmacare-rag-vector-store`. <br> - Configured the collection type as Vector Search. <br> - Configured network policy so OpenSearch can be accessed privately through VPC Endpoint. <br> - Configured data access policy so the AI Lambda role can create indexes, write documents, and query vectors. | 30/06/2026 | 30/06/2026 |
| 6 | - Created IAM Role `pharmacare-rag-lambda-role` for AI Lambda functions. <br> - Granted permissions for CloudWatch Logs, VPC access, S3 read access, Bedrock Runtime access, and OpenSearch Serverless access. <br> - Created Lambda function `pharmacare-rag-indexing`. <br> - Configured environment variables for S3 bucket, knowledge prefix, embedding model, OpenSearch endpoint, index name, and AWS region. <br> - Ran Lambda Indexing to process knowledge files from S3. | 01/07/2026 | 01/07/2026 |
| 7 | - Created Lambda function `pharmacare-rag-chatbot`. <br> - Configured chatbot logic to receive a user question, create question embedding, query OpenSearch Vector Store, and generate an answer from the retrieved context. <br> - Added `ENABLE_LLM` environment variable to support both LLM answer mode and RAG search-only mode. <br> - Created API Gateway route `POST /chat`. <br> - Integrated the chatbot API with the frontend chatbot component. <br> - Tested chatbot questions related to medicine information, product suggestions, pharmacy policy, and FAQ. | 02/07/2026 | 02/07/2026 |

### Week 11 Achievements

* Completed the AI/RAG layer for the **PharmaCare AI** system.

* Created S3 bucket `pharmacare-knowledge-docs-phu-2026` for internal knowledge documents.

* Organized knowledge documents under the `knowledge/` prefix, including:

  * `products`
  * `faq`
  * `medical-guides`
  * `health-articles`
  * `safety`
  * `indexes`

* Prepared approximately 250 knowledge files for the chatbot.

* Included around 193 product-related files for medicines and healthcare products.

* Configured Amazon Bedrock for AI processing.

* Used `cohere.embed-multilingual-v3` to create vector embeddings.

* Prepared Amazon Nova Micro as the LLM model for natural language response generation when `ENABLE_LLM=true`.

* Created OpenSearch Serverless collection `pharmacare-rag-vector-store` as the vector store.

* Configured OpenSearch Serverless as a Vector Search collection.

* Configured private network access for the AI layer using:

  * S3 Gateway Endpoint
  * Bedrock Runtime VPC Endpoint
  * OpenSearch Serverless VPC Endpoint

* Created IAM Role `pharmacare-rag-lambda-role` for AI Lambda functions.

* Applied least-privilege permissions so Lambda can:

  * Write logs to CloudWatch
  * Run inside VPC
  * Read knowledge documents from S3
  * Call Bedrock Runtime
  * Access OpenSearch Serverless

* Created Lambda Indexing to process knowledge documents.

* Lambda Indexing was able to:

  * Read `.txt` files from S3
  * Split document content into smaller chunks
  * Generate embeddings using Amazon Bedrock
  * Store vector data in OpenSearch Serverless

* Successfully indexed 250 files and created 1186 chunks in OpenSearch Vector Store.

* Created Lambda Chatbot to process user questions.

* Lambda Chatbot was able to:

  * Receive a question from the user
  * Generate embedding for the question
  * Search related knowledge in OpenSearch
  * Return an answer based on internal pharmacy documents

* Added `ENABLE_LLM=false` mode to reduce token usage when Bedrock LLM quota is limited.

* Created API Gateway route `POST /chat` for chatbot requests.

* Integrated chatbot into the frontend interface.

* Tested chatbot with medicine-related questions such as product usage, fever-related product suggestions, diarrhea-related product suggestions, pharmacy FAQ, and policy questions.

* Completed week 11 with a working AI/RAG chatbot pipeline connected to S3, Bedrock, OpenSearch Serverless, Lambda, API Gateway, and frontend.