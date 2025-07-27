# Design Document

## Overview

This design outlines the systematic refactoring of Chinese variable names in the CF-Workers-SUB project to English equivalents. The refactoring will maintain all existing functionality while improving code readability and international accessibility.

## Architecture

The refactoring will follow a systematic approach:

1. **Variable Mapping**: Create a comprehensive mapping of Chinese variables to English equivalents
2. **Incremental Replacement**: Replace variables in logical groups to maintain functionality
3. **Testing**: Verify functionality after each group of changes
4. **Documentation Update**: Update comments and documentation to reflect new variable names

## Components and Interfaces

### Core Variable Categories

#### 1. Subscription-related Variables
- `访客订阅` → `guestSubscription`
- `重新汇总所有链接` → `aggregatedLinks`
- `自建节点` → `customNodes`
- `订阅链接` → `subscriptionUrls`
- `订阅格式` → `subscriptionFormat`
- `订阅转换URL` → `conversionUrl`
- `订阅链接数组` → `subscriptionUrlArray`
- `请求订阅响应内容` → `subscriptionResponse`
- `订阅内容` → `subscriptionContent`
- `订阅转换URLs` → `conversionUrls`
- `异常订阅` → `invalidSubscriptions`

#### 2. User Agent and Request Variables
- `追加UA` → `appendedUserAgent`

#### 3. Function Names
- `迁移地址列表` → `migrateAddressList`

#### 4. String Literals and Messages
- Update Chinese text in Telegram messages
- Update Chinese text in HTML templates
- Update Chinese comments

### Variable Naming Conventions

All new variable names will follow:
- **camelCase** for JavaScript variables
- **Descriptive names** that clearly indicate purpose
- **Consistent patterns** for similar concepts
- **English-only** characters

## Data Models

### Variable Mapping Table

| Chinese Variable | English Equivalent | Type | Description |
|------------------|-------------------|------|-------------|
| `访客订阅` | `guestSubscription` | string | Guest subscription token |
| `重新汇总所有链接` | `aggregatedLinks` | array | All aggregated links |
| `自建节点` | `customNodes` | string | Custom node configurations |
| `订阅链接` | `subscriptionUrls` | string | Subscription URLs |
| `订阅格式` | `subscriptionFormat` | string | Subscription format type |
| `订阅转换URL` | `conversionUrl` | string | URL for subscription conversion |
| `订阅链接数组` | `subscriptionUrlArray` | array | Array of subscription URLs |
| `请求订阅响应内容` | `subscriptionResponse` | array | Response content from subscription requests |
| `订阅内容` | `subscriptionContent` | array | Processed subscription content |
| `订阅转换URLs` | `conversionUrls` | string | URLs for conversion service |
| `异常订阅` | `invalidSubscriptions` | string | Invalid subscription entries |
| `追加UA` | `appendedUserAgent` | string | User agent string to append |
| `迁移地址列表` | `migrateAddressList` | function | Function to migrate address list |

## Error Handling

### Refactoring Safety Measures

1. **Incremental Changes**: Make changes in small, testable increments
2. **Backup Strategy**: Maintain original file backup during refactoring
3. **Functionality Verification**: Test core functionality after each change group
4. **Rollback Plan**: Ability to revert changes if issues are discovered

### Error Prevention

1. **Consistent Naming**: Use established patterns for similar variables
2. **Scope Verification**: Ensure all variable references are updated
3. **String Literal Updates**: Update all string references to variables
4. **Comment Synchronization**: Keep comments in sync with variable changes

## Testing Strategy

### Testing Approach

1. **Unit-level Testing**: Test individual functions after variable changes
2. **Integration Testing**: Verify subscription processing workflow
3. **End-to-end Testing**: Test complete subscription conversion process
4. **Regression Testing**: Ensure no functionality is broken

### Test Cases

1. **Subscription Processing**: Verify base64 and URL subscription handling
2. **User Agent Detection**: Test format detection based on user agent
3. **Error Handling**: Verify error cases still work correctly
4. **HTML Generation**: Test admin interface functionality
5. **Telegram Integration**: Verify messaging functionality

### Validation Criteria

- All existing functionality remains intact
- No runtime errors introduced
- Code passes JavaScript linting
- All variable references are consistent
- Comments and documentation are updated

## Implementation Phases

### Phase 1: Core Subscription Variables
Focus on main subscription processing variables that are used throughout the codebase.

### Phase 2: Helper and Utility Variables
Update supporting variables and function names.

### Phase 3: String Literals and Messages
Update Chinese text in messages, comments, and HTML templates.

### Phase 4: Final Verification
Comprehensive testing and cleanup of any remaining Chinese text.