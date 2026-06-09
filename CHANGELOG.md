# Changelog

## v1.0.1 - 2024-01-15

### Features Added
- ✨ New invoice generation API endpoint
- 📊 Enhanced billing dashboard with real-time metrics
- 🔄 Automatic retry mechanism for failed transactions

### Bug Fixes
- 🐛 Fixed decimal precision in billing calculations
- 🔧 Corrected timezone handling for international customers
- ⚡ Resolved memory leak in background processing

### Performance Improvements
- 🚀 50% faster invoice generation
- 💾 Reduced database query time by 30%
- 📈 Optimized API response times

### Technical Changes
- Updated dependencies to latest stable versions
- Added comprehensive error logging
- Improved test coverage to 85%

### Database Changes
- Added `invoices` table with foreign key to `accounts`
- Added index on `billing_records.customer_id` for better query performance
- Migration script: `db/migrations/001_add_invoice_table.sql`

### API Changes
- **NEW**: `POST /api/v1/invoices` - Generate new invoice
- **NEW**: `GET /api/v1/invoices/{id}` - Retrieve invoice details
- **UPDATED**: `GET /api/v1/billing/summary` - Now includes YTD totals

### Breaking Changes
None - Fully backward compatible

### Security Updates
- Updated authentication middleware
- Added rate limiting to prevent abuse
- Implemented request validation

---

## v1.0.0 - 2024-01-01

Initial release with core billing functionality.
