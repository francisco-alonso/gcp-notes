## Cloud IAM

**Cloud Identity and Access Management (IAM)** provides centralized access control across Google Cloud resources. It allows administrators to define who has what level of access to resources.

### 1. List IAM policies for a project
```sh
gcloud projects get-iam-policy PROJECT_ID
```
**Explanation:** Retrieves the IAM policy for a specified project.

**Options:**
- `--format=FORMAT` → Outputs in different formats (e.g., `json`, `yaml`).

### 2. Assign a role to a user
```sh
gcloud projects add-iam-policy-binding PROJECT_ID --member=MEMBER --role=ROLE
```
**Explanation:** Grants a specific role to a user, service account, or group.

**Options:**
- `--member=MEMBER` → Defines the user (`user:EMAIL`, `serviceAccount:EMAIL`, `group:EMAIL`).
- `--role=ROLE` → Specifies the IAM role (`roles/editor`, `roles/viewer`).

### 3. Remove a role from a user
```sh
gcloud projects remove-iam-policy-binding PROJECT_ID --member=MEMBER --role=ROLE
```
**Explanation:** Removes an assigned role from a user, service account, or group.

### 4. List available IAM roles
```sh
gcloud iam roles list
```
**Explanation:** Lists all predefined IAM roles available in Google Cloud.

### 5. List IAM roles for a specific project
```sh
gcloud projects get-iam-policy PROJECT_ID --flatten="bindings[].role" --format='table(bindings.role)'
```
**Explanation:** Displays all roles assigned within a project.

### 6. Create a custom IAM role
```sh
gcloud iam roles create ROLE_ID --project=PROJECT_ID --title=TITLE --description=DESCRIPTION --permissions=PERMISSIONS --stage=STAGE
```
**Explanation:** Creates a custom IAM role with specified permissions.

**Options:**
- `--permissions=PERMISSIONS` → Comma-separated list of permissions.
- `--stage=STAGE` → Defines role lifecycle stage (`ALPHA`, `BETA`, `GA`).

### 7. Update an existing custom IAM role
```sh
gcloud iam roles update ROLE_ID --project=PROJECT_ID --permissions=NEW_PERMISSIONS
```
**Explanation:** Modifies permissions for an existing custom IAM role.

### 8. Delete a custom IAM role
```sh
gcloud iam roles delete ROLE_ID --project=PROJECT_ID
```
**Explanation:** Deletes a custom IAM role.

### 9. Create a service account
```sh
gcloud iam service-accounts create SERVICE_ACCOUNT_ID --display-name="DISPLAY_NAME"
```
**Explanation:** Creates a new service account.

### 10. List service accounts in a project
```sh
gcloud iam service-accounts list --project=PROJECT_ID
```
**Explanation:** Lists all service accounts within a project.

### 11. Assign a role to a service account
```sh
gcloud projects add-iam-policy-binding PROJECT_ID --member=serviceAccount:SERVICE_ACCOUNT_EMAIL --role=ROLE
```
**Explanation:** Grants a specific role to a service account.

### 12. Generate service account keys
```sh
gcloud iam service-accounts keys create KEY_FILE --iam-account=SERVICE_ACCOUNT_EMAIL
```
**Explanation:** Creates a key file for a service account.

### 13. Delete a service account key
```sh
gcloud iam service-accounts keys delete KEY_ID --iam-account=SERVICE_ACCOUNT_EMAIL
```
**Explanation:** Deletes a specific key from a service account.

### 14. Delete a service account
```sh
gcloud iam service-accounts delete SERVICE_ACCOUNT_EMAIL
```
**Explanation:** Permanently removes a service account.

### 15. Enable workload identity for a service account
```sh
gcloud iam service-accounts add-iam-policy-binding SERVICE_ACCOUNT_EMAIL --role=roles/iam.workloadIdentityUser --member=MEMBER
```
**Explanation:** Grants workload identity access to a service account.

---

