# GitHub Workflow Dependencies Demo

This repository demonstrates various methods of managing workflow dependencies in GitHub Actions. The examples provided cover a wide range of scenarios to help you understand and implement dependent workflows effectively.

## Table of Contents

- [Introduction](#introduction)
- [Workflow Examples](#workflow-examples)
  - [1. Manual Workflow Example](#1-manual-workflow-example)
  - [2. Reusable Workflow Simple Example](#2-reusable-workflow-simple-example)
  - [3. Reusable Workflow with Inputs and Secrets](#3-reusable-workflow-with-inputs-and-secrets)
  - [4. Using Outputs from Reusable Workflow](#4-using-outputs-from-reusable-workflow)
  - [5. Nesting Reusable Workflows](#5-nesting-reusable-workflows)
  - [6. Composite Action Example](#6-composite-action-example)
  - [7. Sequential Workflows](#7-sequential-workflows)
  - [8. Sequential Workflows Based on Conclusion](#8-sequential-workflows-based-on-conclusion)
  - [9. Using Data from Triggering Workflow](#9-using-data-from-triggering-workflow)
  - [10. Branch Based Workflow Execution](#10-branch-based-workflow-execution)
- [License](#license)

## Introduction

This repository provides a comprehensive guide on creating and managing dependent workflows using GitHub Actions. By understanding these examples, you can create more efficient and maintainable CI/CD pipelines.

## Workflow Examples

### 1. Manual Workflow Example

This example demonstrates a workflow that can be manually triggered using the `workflow_dispatch` event. It is useful for testing or manual deployment scenarios.

### 2. Reusable Workflow Simple Example

This example shows how to call a reusable workflow from a parent workflow. Reusable workflows help in modularizing and reusing common workflow steps across different workflows.

### 3. Reusable Workflow with Inputs and Secrets

This example demonstrates how to pass inputs and secrets to a reusable workflow. It allows for more dynamic and secure workflows by externalizing input parameters and secrets.

### 4. Using Outputs from Reusable Workflow

This example shows how to use outputs from a reusable workflow in the parent workflow. It helps in chaining workflows together by passing data between them.

### 5. Nesting Reusable Workflows

This example demonstrates how to nest reusable workflows within each other. It showcases how complex workflows can be broken down into simpler, reusable components.

### 6. Composite Action Example

This example demonstrates how to create and use a composite action. Composite actions are a way to bundle multiple steps into a single reusable action, which can be used across different workflows.

### 7. Sequential Workflows

This example demonstrates how to create sequential workflows using the `workflow_run` event. One workflow triggers another workflow upon its completion.

### 8. Sequential Workflows Based on Conclusion

This example shows how to run different workflows based on the conclusion of a previous workflow (success or failure). It is useful for implementing different paths of execution based on the outcome of a workflow.

### 9. Using Data from Triggering Workflow

This example demonstrates how to pass data from one workflow to another using artifacts. It shows how to upload data as an artifact in one workflow and download it in another workflow.

### 10. Branch Based Workflow Execution

This example demonstrates how to run workflows based on the branch of the triggering event. It shows how to create workflows that are specific to different branches (e.g., `develop` and `master`).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Repository Structure

- **1-manual-workflow-example.yml**: Demonstrates a manually triggered workflow.
- **2-reusable-workflow-simple-example--parent-workflow.yml**: Parent workflow for calling a simple reusable workflow.
- **2-reusable-workflow-simple-example--child-workflow.yml**: Child workflow for a simple reusable workflow.
- **3-reusable-workflow-with-inputs-and-secrets--parent-workflow.yml**: Parent workflow passing inputs and secrets.
- **3-reusable-workflow-with-inputs-and-secrets--child-workflow.yml**: Child workflow receiving inputs and secrets.
- **4-using-outputs-from-reusable-workflow--parent-workflow.yml**: Parent workflow using outputs from a child workflow.
- **4-using-outputs-from-reusable-workflow--child-workflow.yml**: Child workflow providing outputs.
- **5-nesting-reusable-workflows--caller-workflow.yml**: Caller workflow demonstrating nested reusable workflows.
- **5-nesting-reusable-workflows--called-workflow-1.yml**: First level of nested reusable workflows.
- **5-nesting-reusable-workflows--called-workflow-2.yml**: Second level of nested reusable workflows.
- **5-nesting-reusable-workflows--called-workflow-3.yml**: Third level of nested reusable workflows.
- **6-composite-action--caller.yml**: Demonstrates using a composite action.
- **6-composite-action--definition/action.yml**: Definition of a composite action.
- **7-sequential-workflows-first.yml**: First workflow in a sequential workflow setup.
- **7-sequential-workflows-second.yml**: Second workflow triggered by the completion of the first workflow.
- **8-sequential-workflows-based-on-conclusion--success.yml**: Workflow that succeeds.
- **8-sequential-workflows-based-on-conclusion--failure.yml**: Workflow that fails.
- **8-sequential-workflows-based-on-conclusion--final.yml**: Final workflow running based on the conclusion of previous workflows.
- **9-using-data-from-triggering-workflow--first.yml**: First workflow generating data.
- **9-using-data-from-triggering-workflow--second.yml**: Second workflow using data from the first workflow.
- **10-branch-based-workflow-execution--develop.yml**: Workflow running on the develop branch.
- **10-branch-based-workflow-execution--master.yml**: Workflow running on the master branch.
- **10-branch-based-workflow-execution--final.yml**: Final workflow running if previous workflow ran on the develop branch.

For detailed descriptions of each example, please refer to the [Wiki](https://github.com/olsido/github-workflow-dependencies-demo/wiki).
