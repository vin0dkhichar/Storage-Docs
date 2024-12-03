# OpenG2P: Storage
The Storage Backend module integrates with various storage solutions, allowing Odoo to manage and store files effectively across different backends. The Storage Backend S3 integration facilitates storing files in Amazon S3, while the Storage File module ensures the smooth handling of file data, both locally and remotely. Together, these modules provide a robust and scalable solution for file storage, management, and access, supporting a wide range of storage strategies from local servers to cloud solutions like Amazon S3.

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

## Source Code
[https://github.com/OpenG2P/storage/tree/17.0](https://github.com/OpenG2P/storage/tree/17.0)
