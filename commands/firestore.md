**Firestore** is a NoSQL document database that simplifies storing, syncing, and querying data for mobile, web, and server development. It offers real-time synchronization and offline support.

### 1. List all Firestore databases
```sh
gcloud firestore databases list
```
**Explanation:** Lists all Firestore databases in the current project.

### 2. Create a new Firestore database
```sh
gcloud firestore databases create --location=LOCATION --type=DATABASE_TYPE
```
**Explanation:** Creates a Firestore database.

**Options:**
- `--location=LOCATION` → Defines the database location (e.g., `us-central1`).
- `--type=DATABASE_TYPE` → Specifies database type (`firestore-native`, `datastore-mode`).

### 3. Delete a Firestore database
```sh
gcloud firestore databases delete DATABASE_ID
```
**Explanation:** Deletes a specified Firestore database.

### 4. Export Firestore data to Cloud Storage
```sh
gcloud firestore export gs://BUCKET_NAME
```
**Explanation:** Exports all Firestore data to a Cloud Storage bucket.

### 5. Import Firestore data from Cloud Storage
```sh
gcloud firestore import gs://BUCKET_NAME/EXPORT_PREFIX
```
**Explanation:** Imports Firestore data from a Cloud Storage bucket.

### 6. List all Firestore indexes
```sh
gcloud firestore indexes composite list
```
**Explanation:** Lists all composite indexes in Firestore.

### 7. Create a Firestore index
```sh
gcloud firestore indexes composite create --collection-group=COLLECTION --field-config=FIELD_CONFIG
```
**Explanation:** Creates a composite index in Firestore.

### 8. Delete a Firestore index
```sh
gcloud firestore indexes composite delete INDEX_ID
```
**Explanation:** Deletes a specified Firestore index.

### 9. List Firestore rules
```sh
gcloud firestore security-rules list
```
**Explanation:** Lists all Firestore security rules.

### 10. Deploy Firestore rules
```sh
gcloud firestore security-rules deploy --source=RULES_FILE
```
**Explanation:** Deploys Firestore security rules from a specified file.

### 11. Get Firestore rules
```sh
gcloud firestore security-rules get
```
**Explanation:** Retrieves Firestore security rules.

### 12. Enable Firestore in Datastore mode
```sh
gcloud alpha firestore databases create --type=datastore-mode
```
**Explanation:** Enables Firestore in Datastore mode.

### 13. List Firestore operations
```sh
gcloud firestore operations list
```
**Explanation:** Lists ongoing Firestore operations.

### 14. Cancel a Firestore operation
```sh
gcloud firestore operations cancel OPERATION_ID
```
**Explanation:** Cancels a specified Firestore operation.

### 15. Describe a Firestore operation
```sh
gcloud firestore operations describe OPERATION_ID
```
**Explanation:** Retrieves details of a Firestore operation.

---
