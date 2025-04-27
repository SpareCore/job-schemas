# Job Schemas

## Overview
Job Schemas is the foundation layer of the SpareCore distributed computing system. It defines standardized schemas, message formats, and contracts to ensure seamless communication between all components of the system.

## Purpose
- Provides a shared language for job definitions across the entire SpareCore ecosystem
- Ensures data consistency and compatibility between node agents and the job server
- Establishes standard formats for common distributed computing tasks

## Key Components
- **Schema Definitions**: JSON/YAML/Protocol Buffer definitions for various job types
- **Message Protocols**: Standardized message formats for system communication
- **Job Types**: Predefined templates for common tasks:
  - OCR processing
  - PDF parsing and extraction
  - Image processing
  - Text analysis
  - General computation tasks

## Schema Files
- **job-schema.json**: Base schema for all job types
- **ocr-job-schema.json**: Schema for OCR jobs
- **pdf-parse-job-schema.json**: Schema for PDF parsing jobs
- **message-schema.json**: Base schema for all system messages
- **node-messages.json**: Message schemas for node registration, heartbeat, and status updates
- **job-messages.json**: Message schemas for job requests, assignments, status updates, and results
- **system-messages.json**: Message schemas for system notifications and error reports
- **config-schema.yaml**: YAML schema for system configuration

## Usage
Job Schemas are imported and utilized by both the Node Agent and Job Server components, acting as the binding contract that ensures proper communication across the distributed system.

## Technical Details
- **Tech Stack**: JSON, YAML
- Language-agnostic schema definitions
- Versioned contracts to enable backward compatibility
- Validation rules for data integrity
- Extension interfaces for custom job definitions

## Development
When adding new job types or modifying existing schemas, ensure all changes maintain compatibility with existing node agents and server implementations.

## Examples
Each schema file contains comprehensive examples and descriptions of all fields. To add a new job type:

1. Create a new job schema file following the pattern of existing job types
2. Update the `job_type` enum in `job-schema.json` to include the new job type
3. Add the new job type to the `capabilities` array in the node registration message
4. Update the job message schemas to reference the new job type