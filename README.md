# Job Schemas

## Overview
Job Schemas is the foundation layer of the GoPine distributed computing system. It defines standardized schemas, message formats, and contracts to ensure seamless communication between all components of the system.

## Purpose
- Provides a shared language for job definitions across the entire GoPine ecosystem
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