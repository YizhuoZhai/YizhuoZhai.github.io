# A Comprehensive Guide to Artifact Evaluation in Computer Science

## Introduction
In recent conferences in the field of computer science, artifact evaluation has become an integral part of facilitating further research. However, the process can often be lengthy and complicated for both authors and reviewers, primarily because authors may struggle with presenting their research prototypes effectively. In this article, we aim to provide guidance for successfully navigating the artifact evaluation process.

## The Three Criteria
Every artifact evaluation typically involves three criteria: availability, functionality, and reproducibility. Let's delve into each criterion and understand what it entails.

### 1. Availability
Availability refers to whether the artifact is publicly accessible under a permissive license. To publish the software, there are various options available, such as licensing a GitHub repository. At the very least, you need to provide a license to demonstrate that the software is indeed accessible.

### 2. Functionality
Functionality assesses whether the artifact builds and runs successfully using the provided instructions. While the common practice involves installing dependencies using shell scripts, this can often lead to complications due to the default operating system already having some dependencies. To overcome this challenge, it is highly recommended to include a Dockerfile, which provides a containerized environment for seamless setup and execution.

### 3. Reproducibility
Reproducibility focuses on whether the reviewer can replicate the results as described in the paper. To meet this criterion, authors should create step-by-step tutorials that enable result reproduction. It is not necessary to include every single step from the experiments; instead, aim to provide an end-to-end usage guide. Ideally, package everything within scripts so that reviewers can execute them, obtain the results, and understand their significance based on the explanations in the paper.

## Conclusion
By following these guidelines, authors can increase their chances of successfully passing artifact evaluation. Ensuring availability, functionality, and reproducibility of the artifact is essential for fostering transparency and enabling further research in the field of computer science.

Remember, artifact evaluation is an opportunity to showcase your research prototype effectively and contribute to the advancement of knowledge in your domain.
