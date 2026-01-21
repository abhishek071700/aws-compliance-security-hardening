# DynamoDB KMS Encryption (Reference Notes)

## Goals
- strengthen data-at-rest encryption baseline

## Strategy
- New tables: enable KMS CMK encryption
- Existing tables: migration plan (export/import or streams-based)
