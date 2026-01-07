# Essential Git Terminology

To understand how Git works, it is fundamental to know some key terms:

## SHA-1 (Secure Hash Algorithm 1)

SHA-1 is a **cryptographic algorithm** that generates a 40-digit *hash*. In Git, it is used to uniquely identify each object (files, directories, commits). Any change, no matter how small, in the content of a file will result in a completely different SHA-1, ensuring data integrity and traceability.

## Blob (Binary Large Object)

A **Blob** represents the content of an individual file stored in Git. It holds the raw content of the file, without metadata such as name or permissions. Each time a file is modified and saved, a new blob is created.

## Tree

A **Tree** is an object that functions like a directory. It lists blobs (files) and other trees (subdirectories), forming the hierarchical structure of the repository. A tree points to the blobs and trees it contains, along with their names and permissions.

## Commit

A **Commit** is a snapshot of the repository at a given moment. It points to a root tree object that represents the complete state of the project at that commit. Additionally, a commit contains important metadata such as:

- **Message**: A description of what was changed.
- **Author**: Who made the change.
- **Date**: When the change was made.
- **Parent**: Reference to the previous commit, forming the project's history.

These elements are the basis for version control in Git, allowing the project's history to be maintained efficiently and securely.
