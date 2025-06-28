# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is the wcag-as-json project - a JSON formatted version of WCAG 2.2 (Web Content Accessibility Guidelines). It provides WCAG standards in a structured, machine-readable format for easy integration into other tools and documentation.

## Commands

### Validation
- **Validate all JSON files**: `npm test` or `npm run validate`
- **Validate specific files**:
  - wcag.json only: `npm run validate:json`
  - wcag-schema.json only: `npm run validate:schema`

### Formatting
- **Format JSON files**: `npm run format`
- **Check formatting**: `npm run format:check`

### Development Setup
- **Install dependencies**: `npm install`
- **Node.js requirement**: >= 14.0.0

## Architecture

### Project Structure
- `wcag.json` - Main data file containing WCAG 2.2 standards
- `wcag-schema.json` - JSON Schema for validating the wcag.json structure
- `package.json` - Node.js project configuration

### Data Structure
The WCAG JSON follows a hierarchical structure:
```
Principles (4) → Guidelines → Success Criteria
```

Each Success Criterion includes:
- `ref_id`: Unique identifier (e.g., "1.1.1")
- `title`: SC name
- `description`: Full text of the criterion
- `url`: Link to official WCAG documentation
- `level`: Conformance level (A, AA, or AAA)
- `special_cases`: Additional considerations with types:
  - `exception`: Creates an exception where SC doesn't apply
  - `at_least_one`: At least one special case must apply
  - `all_true`: All special cases must apply
- `notes`: Additional notes
- `references`: Links to "How to Meet" and "Understanding" documents


## Important Notes

- This is a reference data project - modifications should focus on accuracy of WCAG content
- All JSON files must pass validation against the schema
- The project includes WCAG 2.2 content (Copyright © W3C®)
