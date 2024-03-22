# Latitude Restack repository

Welcome to the Latitude Restack Starter Repository! This repository serves as a template for building your own Latitude using Restack.

## About Restack

[Restack](https://www.restack.io/) is the platform to run your favorite open source products: Build your custom image, scale cost-efficiently with no downtime and upgrade seamlessly to the latest release.

## Features

This starter repository includes:

- A pre-configured Dockerfile for building a Latitude image tailored for Restack deployments.
- A pre-configured sample-netflix.
- A docker-compose.yaml file for developing in a local environment. This file is not used for Restack builds, just for you to work on locally.

## Getting started

[Deploy Latitude on Restack](https://console.restack.io/onboarding/store/3a03a58b-0225-42ae-b21e-c36203fd146c)

Navigate to your Latitude application page and set up `Build custom image with GitHub` ![Build Custom Image with GitHub](images/build_custom_image.png)

Once set up, every time you make a new commit to the branch defined in the previous step, Restack will automatically build and provision your image at the same URL endpoint.

## Generating a preview environment

To create preview environments before merging into production, follow these steps:

1. Create a Stack and enable CI/CD previews: ![enable cicd previews](images/enable_cicd.png)
2. Opening a pull request will automatically generate a preview environment.
3. Merging the pull request will update your initial Latitude application with the new image at the same URL endpoint.
