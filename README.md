# DaemonRS: Building Git from Scratch with Rust

This project is a learning exercise to build a simplified Git implementation from the ground up using the Rust programming language. The primary goal is to understand the core concepts and inner workings of Git by re-creating its fundamental features.

## Project Goals

*   **Understand Git's Internals:** Delve into the data structures and algorithms that power Git, such as the object database (blobs, trees, commits), the index (staging area), and branching models.
*   **Learn Rust:** Apply and expand Rust knowledge in a significant, real-world project, focusing on concepts like ownership, lifetimes, error handling, and concurrency.
*   **Create a Functional Git Clone:** Develop a command-line tool that mimics the basic functionality of Git, capable of initializing repositories, tracking changes, committing files, and managing branches.

## Features and Components

The project will be built in phases, with each phase focusing on a specific set of Git features.

### Phase 1: The Core - Git Objects and Repository Initialization

*   **`init` Command:** Create the basic repository structure (`.git` directory, `objects`, `refs`, `HEAD`).
*   **Object Database:**
    *   **Blobs:** Store file content.
    *   **Trees:** Represent directory structures.
    *   **Commits:** Capture snapshots of the repository's state.
*   **Hashing:** Use SHA-1 to create unique identifiers for objects.
*   **Object Serialization/Deserialization:** Read and write Git objects to the filesystem.

### Phase 2: The Staging Area and Committing

*   **The Index/Staging Area:** Implement the mechanism for staging changes before committing.
*   **`add` Command:** Add file contents to the index.
*   **`commit` Command:** Create a new commit object from the current index.
*   **`status` Command:** Show the state of the working directory and the staging area.

### Phase 3: Branching and History

*   **`branch` Command:** Create, list, and delete branches.
*   **`checkout` Command:** Switch between branches, updating the working directory.
*   **`log` Command:** Display the commit history of the current branch.

### Phase 4: Merging (Advanced)

*   **`merge` Command:** Implement a basic merge strategy to combine the histories of two branches. This will likely be limited to fast-forward merges initially, with more complex strategies as a stretch goal.

### Phase 5: Remotes (Stretch Goal)

*   **`clone` Command:** Fetch a repository from a remote URL.
*   **`fetch` Command:** Download objects and refs from another repository.
*   **`push` Command:** Upload objects and refs to another repository.
*   **`pull` Command:** Fetch from and integrate with another repository or a local branch.

## Projected Timeline

This timeline is an estimate and may change as the project evolves. It is designed for a learning pace, with time allocated for research and experimentation.

| Phase | Description                               | Estimated Time |
|-------|-------------------------------------------|----------------|
| **1** | **Foundations & Core Objects**            | 3-4 Weeks      |
|       | Research Git's data model                 |                |
|       | Implement `init` command                  |                |
|       | Implement blob, tree, and commit objects  |                |
| **2** | **Staging and Committing**                | 3-4 Weeks      |
|       | Implement the index/staging area file     |                |
|       | Implement `add` and `commit` commands     |                |
|       | Implement a basic `status` command        |                |
| **3** | **Branching and History**                 | 2-3 Weeks      |
|       | Implement `branch` and `checkout` commands|                |
|       | Implement the `log` command               |                |
| **4** | **Merging**                               | 2-3 Weeks      |
|       | Research merge strategies                 |                |
|       | Implement fast-forward merges             |                |
| **5** | **Remotes (Stretch Goal)**                | 4+ Weeks       |
|       | Research Git's network protocols          |                |
|       | Implement `clone` and `fetch`             |                |
|       | Implement `push` and `pull`               |                |

## Getting Started

*(This section will be updated as the project becomes functional.)*

1.  Clone the repository: `git clone https://github.com/your-username/DaemonRS.git`
2.  Navigate to the project directory: `cd DaemonRS`
3.  Build the project: `cargo build`
4.  Run the executable: `cargo run -- <command>`

## Contributing

This is a personal learning project, but feedback, suggestions, and contributions are welcome. If you have ideas for improvement or want to fix a bug, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
