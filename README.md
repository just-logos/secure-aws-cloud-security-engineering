# secure-aws-cloud-security-engineering

## Organization Management Account
- Root user is break-glass only and will never perform Terraform activities
- Root user used to create a temporary IAM admin user with MFA for CLI use during bootstrap process
    - The temporary IAM admin user will be retired after AWS Organization is set up to leverage member account level identities

### Organization Management Account Responsibilities

The AWS Organizations management account is reserved for organization-level administration and billing functions. Workloads and application resources should not be deployed in this account.

Tasks intentionally retained in management account:
- AWS Organizations administration
- Account creation and organizational structure
- Billing & AWS Budgets
- Organizational-level configuration
- Root user security tasks

Workloads, application infrastructure, and day-to-day administrative operations are performed in various member accounts.