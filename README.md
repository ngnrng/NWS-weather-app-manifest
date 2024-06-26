# Argo CD Manifest Repository for Weather Forecast CLI

## This repository is being updated via a GitHub Actions workflow in [this](https://github.com/ngnrng/NWS-weather-app-code) repo.

This repository contains Kubernetes manifests for deploying the Weather Forecast CLI application using Argo CD. The application fetches and prints current weather data for a list of cities using the National Weather Service API.

## Repository Structure

The repository is organized into the following directories and files:

- `cronjob.yaml`: Defines a Kubernetes CronJob that periodically runs the Weather Forecast CLI application.
- `namespace.yaml`: Specifies the Kubernetes namespace where the application will be deployed.

## Deployment Overview

The Weather Forecast CLI application is deployed as a CronJob in a Kubernetes cluster. This setup allows the application to run at scheduled times, fetching and printing weather data without manual intervention.

### Namespace

The `namespace.yaml` file defines the namespace for isolating the resources related to the Weather Forecast CLI application. It's recommended to deploy the application in its dedicated namespace to manage resources easily.


## Getting Started

To deploy the Weather Forecast CLI application using Argo CD, follow these steps:

1. ***Install Argo CD***: If you haven't already, install Argo CD in your Kubernetes cluster. Follow the [official Argo CD documentation](https://argo-cd.readthedocs.io/en/stable/getting_started/) for installation instructions.

2. ***Create the Namespace***: Apply the `namespace.yaml` to create the namespace for the application:

3. ***Register the Application with Argo CD***: Register this repository as an application in Argo CD, specifying the path to the directory containing the manifests. Ensure you set the namespace to the one defined in namespace.yaml.

4. ***Sync the Application***: Once registered, sync the application in Argo CD to deploy the Weather Forecast CLI application to your cluster.

   
