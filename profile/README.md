Here’s a customized README for the organization WillMaestro:

---

# Welcome to the WillMaestro Team 🙌

## Repo, GitHub, and Code Conventions

At WillMaestro, we strive for consistency and efficiency in our collaborative efforts. Following these conventions helps streamline our workflow, making it easier for both new and seasoned team members to contribute effectively.

### 1. Repositories

1. **Naming**: Use lowercase letters and hyphens to name repositories, like `my-new-repo`.
2. **Template Usage**: When creating a new repository, use the [template-repository](https://github.com/willmaestro/template-repository) as a base. If you have an existing repository that doesn't use this template, please add our [issue templates](https://github.com/willmaestro/template-repository/tree/main/.github/ISSUE_TEMPLATE) and [pull request template](https://github.com/willmaestro/template-repository/blob/main/.github/pull_request_template.md).
3. **Branch Protection**: Follow the [convention](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/managing-a-branch-protection-rule) of a locked main branch, with separate branches for features and fixes.
4. **Access Control**: Provide repository access to the following WillMaestro teams:
   - **@willmaestro/admin** with **Admin** role.
   - **@willmaestro/writer** with **Write** role. (This includes all WillMaestro developers.)
   - **@willmaestro/reader** with **Read** role.
5. **Merge Settings**: Uncheck **Allow merge commits** and check **Allow squash merging** in the repository's **General** settings.

### 2. Branches

1. **Default Branch**: Code changes should not be made directly to the default branch (e.g., `main`, `develop`, `master`).
2. **Branch Naming Convention**: Follow the `<category/reference/description-in-kebab-case>` format:
   - **`category`**: Choose from `epic`, `feat`, `fix`, `hotfix`, or `test`.
   - **`reference`**: Use the numerical ID of the ticket or `no-ref` if none.
   - **`description-in-kebab-case`**: A short, descriptive phrase in kebab-case.

### 3. Commits

- Follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) standard for commit messages.

### 4. Pull Requests (PRs)

1. **Details**: Fill out the PR template fully, noting core features and changes.
2. **Title Prefix**: Use a prefix like `epic:` or any other type supported by [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).
3. **Issue Linking**: Link the PR to its parent WillMaestro issue.
4. **Testing**: Ensure all tests (unit, integration, e2e) pass before requesting a review.
5. **Reviewers**: Assign appropriate reviewers based on familiarity with the codebase—1 for minor changes, at least 2 for major changes.
6. **Merging**: Only the PR owner should merge the changes after a completed review.

### 5. Tests

1. **Coverage**: Add tests for any new feature or significant fix. Aim for comprehensive coverage of all execution paths (e.g., all `if` branches, `switch` statements).
2. **Types**: Unit tests are required; integration and e2e tests are encouraged if available.

### 6. Code

1. **Security**: Be cautious with credentials when committing files.
2. **Documentation**: Include [Natspec](https://docs.soliditylang.org/en/stable/natspec-format.html) comments for smart contracts and high-level comments as needed.
3. **Cleanliness**: Remove debug code, unnecessary print statements, and comments before committing.
4. **Dependencies**: Review all dependencies to ensure they are currently used and safe. Prefer widely maintained open-source projects.
5. **Linting**: Lint all code before committing. Use git hooks for automated linting on commit.

### 7. Configuration

- **Environment Variables**: Configure software through **Environment Variables**. Include an `env.example` file in the repository to show required environment variables.

### 8. Dockerfile

1. **Requirement**: All services must be available as Docker images due to WillMaestro’s Kubernetes infrastructure.
2. **Responsibilities**: The software author must create a [Dockerfile](https://docs.docker.com/engine/reference/builder/) and provide build/run instructions.
3. **Considerations**:
   - Use [multi-stage builds](https://docs.docker.com/develop/develop-images/multistage-build/) to minimize image size.
   - Prefer exposing port 80 unless there’s a specific need for another port.
   - Use `.dockerignore` to exclude unnecessary files from the build context.
   - Only copy necessary files to the final image stage to keep size down.

### 9. README.md

Each repository must include a README file that details:

- **Purpose**: What the software does.
- **Configuration**: Required configuration parameters and example values.
- **Docker Instructions**: How to build and run the Docker image.
- **Integration**: (If applicable) A diagram and description of how this system interacts with external systems, such as blockchain, APIs, databases, or other services.

---

By adhering to these guidelines, we ensure a cohesive and efficient workflow across all of WillMaestro’s projects. Welcome aboard, and let’s create amazing things together! 🎉