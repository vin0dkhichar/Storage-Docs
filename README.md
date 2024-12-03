# OpenG2P: Storage
The Storage module in OpenG2P provides a comprehensive solution for managing and storing files across various backends, it is robust and flexible. Depending on your infrastructure needs, you can store files locally or integrate with cloud storage solutions like Amazon S3.
## Modules
1. **storage_backend**
   - This module serves as the core framework for integrating different file storage solutions. It enables Odoo to handle file management across various backends, from local servers to cloud storage.

2. **storage_backend_s3**
   - This module specifically focuses on Amazon S3, allowing seamless storage of files in the cloud. It enables Odoo to leverage the scalability, security, and performance of Amazon's cloud storage service for file management.

3. **storage_file**
   - The Storage File module is responsible for handling file data, both locally and remotely. It ensures smooth storage operations, file retrieval, and data access, working seamless with both local storage and cloud-based solutions like S3.

## Feature and functionality
| **Feature** | **Description**  |
| ------- | --- |
| **Storage Backend Configuration** | The Storage Backend module enables the configuration of multiple storage backends, allowing administrators to choose where files will be stored. It supports local storage as well as external cloud solutions like Amazon S3.|
| **Amazon S3 Storage Support** | The StorageBackendS3 integration adds functionality for interacting with Amazon S3, enabling files to be stored and retrieved from a cloud-based S3 bucket. Files are uploaded securely, and URLs are generated for access, with options for public and private access configurations. |
| **File Management with Storage File** | The Storage File module provides a unified approach for handling file data, ensuring that files are properly stored, accessed, and managed within Odoo. It manages metadata such as file size, type, and checksum, providing essential information for file management. The module automatically integrates with both local and S3-based storage, simplifying file interactions. |
| **Dynamic Backend Switching** | Files can be configured to switch between local storage and S3 dynamically based on system settings. If configured for Amazon S3, the files are uploaded to the cloud; otherwise, they are stored locally within Odoo. This dynamic configuration offers flexibility and ensures that storage strategies can be adjusted as needed. |
| **File Metadata Management** | The module ensures that metadata, including file size, MIME type, checksum, and storage location, is managed and retained for each file. Whether files are stored locally or on Amazon S3, the metadata is updated and consistent, allowing users to manage their files effectively. |
| **KeyManager Integration** | KeyManager handles the encryption and decryption of files, providing a centralized approach to manage encryption keys securely. Files stored on S3 are encrypted using the KeyManager service, guaranteeing that only authorized users or systems can access and decrypt the files. |
| **Seamless File Handling** | The integration ensures that files are accessed seamlessly regardless of where they are stored. Whether a file is located in an S3 bucket or on the local server, the access URLs are consistent and can be retrieved without complex configurations. |

## Design notes
   - The StorageBackend, StorageBackendS3, and StorageFile models extend core Odoo functionality, adding custom features for file storage and retrieval. The S3 backend inherits from the main storage backend class and provides the specific logic for interacting with Amazon S3. The StorageFile module simplifies file interactions across both local and remote storage.

## Source Code
[https://github.com/OpenG2P/storage/tree/17.0](https://github.com/OpenG2P/storage/tree/17.0)
