**Cloud Storage** is Google Cloud’s object storage service, allowing users to store and retrieve data across different storage classes for varying availability and pricing needs.

### 1. List all buckets
```sh
gcloud storage buckets list
```
**Explanation:** Lists all storage buckets in the current project.

### 2. Create a new storage bucket
```sh
gcloud storage buckets create BUCKET_NAME --location=LOCATION --storage-class=STORAGE_CLASS
```
**Explanation:** Creates a new storage bucket with a specified location and storage class.

### 3. Delete a storage bucket
```sh
gcloud storage buckets delete BUCKET_NAME
```
**Explanation:** Deletes a specified storage bucket.

### 4. Upload a file to a bucket
```sh
gcloud storage cp FILE_PATH gs://BUCKET_NAME
```
**Explanation:** Uploads a file to the specified Cloud Storage bucket.

### 5. Download a file from a bucket
```sh
gcloud storage cp gs://BUCKET_NAME/FILE_PATH LOCAL_PATH
```
**Explanation:** Downloads a file from Cloud Storage to the local system.

### 6. List objects in a bucket
```sh
gcloud storage ls gs://BUCKET_NAME
```
**Explanation:** Lists all objects within a specified bucket.

### 7. Delete an object from a bucket
```sh
gcloud storage rm gs://BUCKET_NAME/OBJECT_NAME
```
**Explanation:** Deletes a specified object from a Cloud Storage bucket.

### 8. Move an object between buckets
```sh
gcloud storage mv gs://SOURCE_BUCKET/OBJECT_NAME gs://DEST_BUCKET/OBJECT_NAME
```
**Explanation:** Moves an object from one Cloud Storage bucket to another.

### 9. Make an object public
```sh
gcloud storage objects add-iam-policy-binding gs://BUCKET_NAME/OBJECT_NAME --role=roles/storage.objectViewer --member=allUsers
```
**Explanation:** Grants public access to a Cloud Storage object.

### 10. Set lifecycle rules for a bucket
```sh
gcloud storage buckets update BUCKET_NAME --lifecycle-file=FILE_PATH
```
**Explanation:** Updates a bucket with lifecycle rules from a specified file.