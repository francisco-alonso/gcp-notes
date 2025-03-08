**Cloud Billing** in Google Cloud allows users to manage billing accounts, budgets, and invoices. It provides tools for cost control and financial governance.

### 1. List all billing accounts
```sh
gcloud beta billing accounts list
```
**Explanation:** Lists all billing accounts associated with your Google Cloud organization.

### 2. Get billing account details
```sh
gcloud beta billing accounts describe BILLING_ACCOUNT_ID
```
**Explanation:** Shows details about a specific billing account.

### 3. Enable billing for a project
```sh
gcloud beta billing projects link PROJECT_ID --billing-account=BILLING_ACCOUNT_ID
```
**Explanation:** Links a Google Cloud project to a billing account.

### 4. Disable billing for a project
```sh
gcloud beta billing projects unlink PROJECT_ID
```
**Explanation:** Unlinks a Google Cloud project from a billing account.

### 5. List billing export settings
```sh
gcloud beta billing accounts get-iam-policy BILLING_ACCOUNT_ID
```
**Explanation:** Lists IAM policies associated with a billing account.

### 6. Create a budget
```sh
gcloud billing budgets create --billing-account=BILLING_ACCOUNT_ID --display-name=NAME --amount=CURRENCY:VALUE
```
**Explanation:** Creates a new budget for tracking expenses.

### 7. List budgets
```sh
gcloud billing budgets list --billing-account=BILLING_ACCOUNT_ID
```
**Explanation:** Lists all budgets associated with a billing account.

### 8. Describe a budget
```sh
gcloud billing budgets describe BUDGET_ID --billing-account=BILLING_ACCOUNT_ID
```
**Explanation:** Retrieves details of a specified budget.

### 9. Update a budget
```sh
gcloud billing budgets update BUDGET_ID --billing-account=BILLING_ACCOUNT_ID --amount=CURRENCY:VALUE
```
**Explanation:** Updates an existing budget.

### 10. Delete a budget
```sh
gcloud billing budgets delete BUDGET_ID --billing-account=BILLING_ACCOUNT_ID
```
**Explanation:** Deletes a specific budget.

### 11. List all invoices
```sh
gcloud beta billing accounts invoices list --billing-account=BILLING_ACCOUNT_ID
```
**Explanation:** Lists all invoices for a billing account.

### 12. View an invoice
```sh
gcloud beta billing accounts invoices describe INVOICE_ID --billing-account=BILLING_ACCOUNT_ID
```
**Explanation:** Retrieves details of a specific invoice.

### 13. Get billing reports
```sh
gcloud beta billing reports describe --billing-account=BILLING_ACCOUNT_ID
```
**Explanation:** Displays cost reports for a billing account.

### 14. List IAM policy for billing
```sh
gcloud beta billing accounts get-iam-policy BILLING_ACCOUNT_ID
```
**Explanation:** Retrieves the IAM policy for a billing account.

### 15. Set IAM policy for billing
```sh
gcloud beta billing accounts set-iam-policy BILLING_ACCOUNT_ID POLICY_FILE
```
**Explanation:** Sets an IAM policy for a billing account.

---