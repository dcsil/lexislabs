# ADR 011: CI/CD Platform

## Context

A good CI/CD framework for our project must have support for testing both code (unit, integration, and end-to-end) and AI, be reasonably easy to set up and maintain, and integrate well with other platforms that we use.

### Options

- GitHub Actions
- CircleCI
- Jenkins

As we already use GitHub, GitHub Actions will be the most easy-to-setup option. In addition to being capable of handling CI/CD, it is also a general automation platform that can satisfy our other automation needs.

As its name suggests, CircleCI is a dedicated CI/CD platform. As discussed by users online, some of its advantages include speed, feature richness, extensibility, and better user interface.

Unlike the previous two, Jenkins is free and open-source. It is highly customizable, scalable, and gives us total control, but these features come at the cost of having to manually set up and manage the entire DevOps infrastructure.

There are other solutions not listed above, notably DevOps solutions provided by cloud providers such as AWS and Microsoft Azure. These are only relevant once we decide on a cloud provider.

## Decision

We will start with GitHub Actions, since it likely already satisfies much of our CI/CD needs at this stage. Its free tier is generous enough to cover our needs, and scaling is handled for us by GitHub.

We will monitor our needs and consider other platforms when necessary, notably when we start focusing on the AI aspects of our product.

## Status

Accepted.

## Consequences

This decision allows us to go ahead with CI setup. We expect future impacts to be manageable even if we do decide to migrate or add additional platforms.