---
title: Development
has_children: false
nav_order: 5
---

# Development

## DVCS
To track the development of our project, I used a GitHub repository and created a dedicated organization called `unibo-dtm-se-2324-graphproject Owner`. The main repository, `GraphProject`, was divided into three main branches:
- **master**: Contains the stable project releases.
- **develop**: Used for active development and contains the latest features and updates.
- **feature/some-feature**: A dedicated branch for developing specific features before merging them into `develop`.

### Branch Usage
While the project primarily used the `master` branch for stable releases, active development occurred across multiple branches, such as `develop` and `feature/some-feature`. New features were implemented in these branches and occasionally merged into `master`. 

Some features and bug fixes were developed directly on `develop` before final integration into `master`, though a more structured branching strategy will be enforced in future iterations to ensure better testing and stability.

 Some examples include:
- `develop`: Contains the latest changes, such as CI/CD workflow configurations.
- `feature/some-feature`: Used for implementing feature-specific changes that are then integrated into `develop`.

### Commit Messages
While I initially intended to follow the Conventional Commit format, some descriptive commit messages were used instead. Examples include:
- "Update index.md in section 7"
- "Resolved merge conflicts"
- "Add detailed Design section"
- "Remove file"

Future development will strictly adhere to Conventional Commit guidelines for clearer commit history tracking.

## Implementation details

The `TutorRecommendation` class and `GraphPlotter` module were not included in the final artifact as distinct components. Instead, their functionality was directly integrated into the backend code.

- **TutorRecommendation Functionality**: Initially planned as a separate class, its logic was embedded within the filtering process for matching tutors based on user preferences.
- **GraphPlotter Functionality**: The graph plotting logic, though not in a separate module, is integrated within the backend and generates graphs dynamically from user input.

In future iterations, I plan to refactor these features into standalone components to enhance modularity and maintainability.
