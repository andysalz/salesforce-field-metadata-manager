# Salesforce Field Metadata Manager

A metadata governance tool for Salesforce that enables bulk export and controlled updates of field labels, descriptions, and help text using Schema Describe and the Metadata API.

## Purpose

Field documentation often becomes outdated in growing Salesforce orgs. This tool provides administrators with a structured way to:

- Export field metadata to CSV for easier review and collaboration with end users
- Update labels, descriptions, and help text in bulk
- Validate changes before deployment
- Execute updates asynchronously using the Metadata API

## Architecture Overview

LWC → Apex Controller → Queueable → Metadata API

Key components:
- Schema Describe for field discovery
- MetadataService wrapper for updates
- CSV utility for export/import handling
- Validation layer for safe updates

## Permissions

Requires:
- Customize Application
- Custom Permission (optional future enhancement)

## Roadmap

- Object and field selection UI
- CSV export engine
- Metadata API integration
- CSV import + validation
- Async update engine
- Production hardening

## Limitations

- Standard field update restrictions apply
- Managed package fields may not be updateable
- Metadata deployments are asynchronous
