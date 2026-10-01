# EcoFlow Studio – Custom Content Generator

## About the Project

EcoFlow Studio is an AI-powered custom content generator designed to create sustainable-product marketing copy.

Users can select a content format, tone, length, and target audience, then provide a product name with optional features and keywords. The application supports multiple content formats, batch generation, saved generation history, usage statistics, and copy/export functionality.

## Content Formats

The generator supports:

- Product descriptions
- Instagram captions
- Email subject lines
- Taglines
- SEO descriptions

## Key Features

- AI-powered content generation
- Custom tone and audience settings
- Short, medium, and long content options
- Batch generation
- Generation history
- Usage statistics
- Copy and export functionality
- API validation
- PostgreSQL data persistence

## How It Works

1. The user selects the desired content format and settings.
2. The product name and optional features or keywords are provided.
3. The browser sends the request to the API.
4. The API validates the request.
5. A format-specific prompt is created.
6. The OpenAI model generates the content.
7. A successful generation is stored in PostgreSQL.
8. The generated content and usage information are returned to the interface.

## AI & API

The application uses OpenAI through Replit AI Integrations.

The implementation uses the `gpt-5-mini` model with a maximum completion limit of 1,024 tokens. The integration keeps provider credentials out of the application source.

## Technology Stack

### Frontend
- React 19
- Vite
- Wouter
- TanStack Query
- React Hook Form
- Zod

### Backend
- Express 5
- TypeScript
- OpenAPI 3.1

### Database
- PostgreSQL
- Drizzle ORM

### AI
- OpenAI
- GPT-5 mini
- Prompt Engineering
- Generative AI

### Development
- Replit
- pnpm

## Prompt Engineering

The generator uses task-specific prompts for each content format.

The prompts combine:

- Product name
- Product features
- Keywords
- Tone
- Target audience
- Content length
- Format-specific requirements

Each content type has its own output guidance to help structure the generated marketing copy.

## Validation & Safeguards

The application validates requests using Zod and the OpenAPI contract before sending them for AI inference.

The documentation also identifies areas for future improvement, including:

- Input length limits
- Output validation
- Moderation
- Prompt-injection protection
- Claim verification
- Human review for consequential claims

## Performance Considerations

The application includes several performance-focused approaches:

- Concurrent batch generation
- Validation before AI inference
- Completion token limits
- Single database insert-and-return operations
- SQL-side usage statistics
- Targeted cache refresh instead of continuous polling

## Current Limitations

The technical documentation identifies several operational limitations:

- No application-level rate limiter
- No retry or queue system
- Batch requests can partially fail
- Generation calls are synchronous
- No independent output moderation or claim verification
- Generation history is not account-scoped
- Input and output token costs are not separately recorded

## Project Documentation

The complete technical documentation is available in this repository.

## What I Learned

- AI-powered application development
- Prompt engineering
- API integration
- Full-stack application architecture
- Request validation
- Database persistence
- OpenAPI API contracts
- Generative AI workflows
- Performance and reliability considerations
- AI safety and operational limitations

## Project Type

Individual Project

## My Project

I independently developed EcoFlow Studio as an AI-powered custom content generator for sustainable-product marketing.

The project involved designing the application workflow, implementing the AI generation process, integrating the API, working with data persistence, and documenting the application's architecture, prompt design, performance considerations, and operational limitations.

