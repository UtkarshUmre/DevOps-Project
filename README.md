# DevOps Project Overview

This DevOps project focuses on deploying an end-to-end application onto a Kubernetes (K8s) cluster with HTTPS and GitOps practices. We utilize GitHub Actions for continuous integration and Argo CD for continuous delivery.

## Key Components

- **HTTPS:** Managed with Cert-Manager and Gateway API, eliminating the need for traditional ingresses while providing additional functionalities.
- **Base Image Security:** To ensure zero CVE (Common Vulnerabilities and Exposures), we use BuildSafe for building secure images.
- **Load Testing:** Conducted using K6 to verify that the application can handle sudden load increases.
- **Programming Language:** The application is written in Go (Golang) and connects to a PostgreSQL database, which is deployed using Cloud Native PG.
- **Artifact Creation:** BuildSafe and KO are used to achieve zero-CVE images, which are then pushed to an OCI registry; for this project, we are using Docker Hub.
- **Monitoring:** Prometheus SDK is utilized for instrumenting the application, while Grafana is used for visualization. Prometheus scrapes the metrics that we have instrumented.

## GitOps and CI/CD

- **GitOps:** Managed with Argo CD.
- **Continuous Integration:** Implemented using GitHub Actions.

## Summary

In summary, this project demonstrates a comprehensive DevOps pipeline for a Golang application, leveraging modern tools and practices to ensure security, scalability, and efficient deployment.
