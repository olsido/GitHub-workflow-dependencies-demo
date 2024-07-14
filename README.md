# GitHub Workflow Dependencies Demo

This repository demonstrates various methods of how GitHub Actions workflows can be dependent on each other. The examples provided will help you understand different scenarios and best practices for managing workflow dependencies in your CI/CD pipeline.

## Table of Contents
* [Introduction](#introduction)
* [Manual Workflow Launch](#manual-workflow-launch)
* [Workflow Scenarios](#workflow-scenarios)
  * [Workflow Calls Another Workflow](#workflow-calls-another-workflow)
  * [Workflow Transfers Control to Another Workflow](#workflow-transfers-control-to-another-workflow)
* [Use Cases](#use-cases)
  * [Passing Parameters](#passing-parameters)
  * [Implication on Branches](#implication-on-branches)
* [License](#license)

## Introduction

This repository provides a comprehensive guide on how to create and manage dependent workflows using GitHub Actions. By understanding these concepts, you can create more efficient and maintainable CI/CD pipelines.

## Manual Workflow Launch

Before diving into workflow dependencies, it is important to learn how to manually launch a workflow. This control is essential for demonstrating various dependencies and testing different scenarios without automatically triggering workflows.

## Workflow Scenarios

### Workflow Calls Another Workflow

In this scenario, one workflow calls another reusable workflow and waits for it to complete before continuing. This is useful for modularizing and reusing common workflow steps.

### Workflow Transfers Control to Another Workflow

Here, the control is entirely transferred to another workflow, and the first workflow does not continue after the called workflow completes. This is useful for sequential workflows where the completion of one triggers the start of another.

## Use Cases

### Passing Parameters

We will demonstrate how to pass parameters between workflows to ensure that the called workflow has the necessary context and inputs from the calling workflow.

### Implication on Branches

Understanding how workflow dependencies affect branch-based workflows is crucial. We will cover the implications and best practices for managing workflow dependencies across different branches.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.