
# FastFoodFast - Development Instructions

## Project Rules

- Inspect the existing architecture before modifying code.
- Follow the project's current architecture and coding conventions.
- Prefer minimal and focused changes.
- Do not refactor unrelated code.
- Do not overwrite changes made by other team members.
- Do not introduce unnecessary dependencies.

## Database Restrictions - CRITICAL

The database must NOT be modified under any circumstances.

- Do not create, modify or delete database tables.
- Do not create or modify migrations.
- Do not modify database schemas, models, seeders or SQL scripts.
- Do not modify database configuration.
- Do not add database columns or relationships.
- Do not change existing database queries for these features.
- Do not introduce new database persistence mechanisms.

Prefer browser localStorage for the requested features.

Use sessionStorage or another existing non-database storage mechanism only when technically necessary.

If a feature cannot be implemented correctly without modifying the database, stop and explain the limitation before making changes.

## Requested Features

### 1. Preserve Shopping Cart After Login

- Prefer localStorage for cart persistence.
- Preserve products and quantities before, during and after login.
- Do not clear the cart during successful authentication.
- Handle existing cart data consistently.
- Store only the necessary cart information.
- Never trust prices stored in localStorage.
- Do not store passwords, authentication tokens or sensitive information in the cart.

### 2. Discount Coupons

- Add coupon registration functionality to the existing admin interface.
- Prefer localStorage for coupon persistence.
- Allow administrators to register coupons through the admin interface.
- Allow the shopping interface to retrieve and validate locally stored coupons.
- Support adding and removing coupons from the cart/order interface.
- Follow the existing interface patterns and visual conventions.
- Do not invent business rules without first presenting them for approval.

## SonarCloud Requirements

- Never introduce new SonarCloud issues.
- Do not disable SonarCloud rules.
- Do not add suppressions or exclusions.
- Do not modify SonarCloud configuration or GitHub Actions workflows.
- Avoid duplication, unnecessary complexity and inaccessible HTML.
- Follow existing code quality conventions.

## Implementation Workflow

1. Inspect the existing architecture.
2. Present the proposed implementation before editing.
3. Implement one feature at a time.
4. Review the complete Git diff.
5. Execute available validation commands.
6. Request an independent review using the reviewer subagent.
7. Correct confirmed issues introduced by the changes.
8. Repeat validation and review.
9. Never commit or push without explicit authorization.

## Final Restrictions

- Do not modify the database.
- Do not implement unrelated features.
- Do not resolve pre-existing issues belonging to other team members.
- Report limitations honestly.
