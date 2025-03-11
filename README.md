# Lab Directory Structure

* **Lab_Root/**
  * **Projects/**
    * **Project_Name_1/**
      * **data/**
        * raw/
        * processed/
        * metadata/
      * **code/**
        * scripts/
        * notebooks/
        * pipelines/
      * **results/**
        * figures/
        * tables/
        * models/
      * manuscript/
      * README.md
    * **Project_Name_2/**
      * ...
  * **People/**
    * LastName_FirstName/
    * Smith_Jane/
    * Smith_John/
    * ...
  * **Resources/**
    * references/
    * databases/
    * standard_datasets/
  * **Admin/**
    * grants/
    * protocols/
    * meetings/
  * **Archive/**
    * **Archived_Projects/**
      * Project_Name_1_YYYY/
      * Project_Name_2_YYYY/
    * **Alumni/**
      * Wang_Dave_YYYY-YYYY/
      * Virgin_Skip_YYYY-YYYY/
      * ...
---
## Directory Explanations

### Projects
Contains all active research projects, each with standardized subdirectories for data, code, results, and documentation.

### People
Individual directories for all current lab members.

### Resources
Shared resources used across multiple projects including references, databases, and standard datasets.

### Admin
Administrative materials including grants, protocols, and meeting notes.

### Archive
- **Archived_Projects**: Completed projects with year of completion
- **Alumni**: Past lab members with their tenure dates
---
# File Management Best Practices

## Naming Conventions

- **Be consistent**: Use snake_case or kebab-case consistently. CamelCase should be avoided, but if used should be consistent
- **Avoid spaces**: Replace spaces with underscores or hyphens
- **Include dates**: Use ISO format (YYYY-MM-DD) when including dates
- **Version numbers**: Include version numbers (v1, v2.3) when applicable
- **Descriptive names**: Files should be self-descriptive without being excessively long

## Data Management

- **Raw data is sacred**: Never modify raw data; always create processed copies
- **Data provenance**: Document the source of all datasets and preprocessing steps
- **Metadata**: Create metadata files (in YAML or JSON) to describe datasets
- **Large files**: Use Git LFS (Large File Storage) for files >100MB. HTCF LFS is for large local data, and Harvard Dataverse is for external hosting.
- **Data validation**: Implement checksums to verify data integrity
- 
## GitHub Integration

- **Repository per project**: Create a separate repository for each major project
- **Branching strategy**:
  - `main` - stable, working code
  - `develop` - integration branch
  - Feature branches for new analyses
- **README files**: Include setup instructions, dependencies, and basic usage
- **GitHub Actions**: Set up automated testing and verification workflows
- **Releases**: Tag significant versions with semantic versioning (v1.0.0)
- **Issues**: Use for tracking tasks, bugs, and future work

## Advanced GitHub Features

- **GitHub Pages**: For project documentation and results sharing
- **Project boards**: For task management and project coordination
- **GitHub Packages**: For storing and sharing lab-developed packages
- **Continuous Integration**: Automatically test code on push

## Code Organization

- **Modular code**: Break code into logical, reusable components
- **Script headers**: Include purpose, author, date, and usage examples in comments
- **Requirements**: Include environment specifications (requirements.txt, environment.yml)
- **Documentation**: Document functions, parameters, and expected outputs

## Reproducibility

- **Environment management**: Use conda or Docker to ensure reproducibility
- **Seed values**: Set and document random seeds
- **Dependency pinning**: Specify exact versions in requirements
- **Notebooks**: RMarkdwon or Jupyter. Consider using nbdev or similar for version control
- **Parameters**: Separate parameters from code in config files

## Automation and Scripts

- **Data processing**: Develop pipelines for standard data transformations
- **Backup scripts**: Implement regular backups for non-GitHub data

## Lab-Specific Considerations

- **Onboarding documents**: Create guides for new lab members
- **Compute resources**: Document procedures for utilizing cluster/cloud resources
- **Collaboration guidelines**: Establish protocols for code sharing and authorship




