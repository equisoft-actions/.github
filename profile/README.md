# Workflows

### [docker-workflows](https://github.com/equisoft-actions/docker-workflows)

#### [Security](https://github.com/equisoft-actions/docker-workflows/blob/main/.github/workflows/security.yml)

Regroups `docker-sast` and `docker-sbom` actions to run on a published Docker image.

### [kotlin-workflows](https://github.com/equisoft-actions/kotlin-workflows)

#### [Micronaut-gradle](https://github.com/equisoft-actions/kotlin-workflows/blob/main/.github/workflows/micronaut-gradle.yml)

Runs various checks for Kotlin code (e.g. static analysis, license check, tests, etc.). Can also build and push docker
images.

### [php-workflows](https://github.com/equisoft-actions/php-workflows)

#### [PHP Library](https://github.com/equisoft-actions/php-workflows/blob/main/.github/workflows/php-library.yml)

Runs various checks for PHP code (e.g. phpcs, psalm).

#### [PHP Security](https://github.com/equisoft-actions/php-workflows/blob/main/.github/workflows/php-security.yml)

Regroups `psalm-taint-analysis` and `composer-sbom` actions.

### [python-workflows](https://github.com/equisoft-actions/python-workflows)

#### [Python Pipenv](https://github.com/equisoft-actions/python-workflows/blob/main/.github/workflows/python-pipenv.yml)

Runs various checks for Python repos that uses Pipenv (e.g. unit tests, type checking, code style, etc.).

#### [Python Security](https://github.com/equisoft-actions/python-workflows/blob/main/.github/workflows/python-security.yml)

Regroups `scan-secrets`, `semgrep` and `pipenv-sbom` actions.

### [js-workflows](https://github.com/equisoft-actions/js-workflows)

#### [Webapp-frontend](https://github.com/equisoft-actions/js-workflows/blob/main/.github/workflows/webapp-frontend.yml)

Runs various checks for JS code (e.g. eslint, stylelint, tests, etc.). Can also build and push docker images.

# Actions

## Misc

### [application-metadata](https://github.com/equisoft-actions/application-metadata)

Resolves common application metadata like the application version or whether it is publishable (by our standards).

### [jacoco-report](https://github.com/equisoft-actions/jacoco-report)

Publishes the JaCoCo report as a comment in the Pull Request.

### [notify-workflow-status](https://github.com/equisoft-actions/notify-workflow-status)

Pushes a whole workflow result to a Slack webhook.

### [with-asdf-vm](https://github.com/equisoft-actions/with-asdf-vm)

Downloads asdf-vm with cache. Initialize JAVA_HOME if java is specified in `.tool-version`.

## Security

### [scan-secrets](https://github.com/equisoft-actions/scan-secrets)

Scans commits for leaked secrets. By default, pull request events will only scan new commits and push events will scan
all commits.

### [semgrep](https://github.com/equisoft-actions/semgrep)

Utilizes Semgrep (SAST) to generate a SARIF report. The report is archived and uploaded to Defect Dojo.

## Docker

### [docker-build-and-push](https://github.com/equisoft-actions/docker-build-and-push)

Builds a container image and optionally push it. Labels and tags will be configured as per the OCI standards.

### [docker-metadata](https://github.com/equisoft-actions/docker-metadata)

Resolves docker metadata such as tags and OCI labels.

### [docker-sast](https://github.com/equisoft-actions/docker-sast)

Utilizes Dockle to generate a SARIF report. The report is archived and uploaded to Defect Dojo.

### [docker-sbom](https://github.com/equisoft-actions/docker-sbom)

Utilizes Tern to generate a SBOM. This SBOM will then be archived and uploaded to Dependency-Track.

### [hadolint](https://github.com/equisoft-actions/hadolint)

Runs Hadolint Dockerfile linting tool.

## Gradle

### [generate-openapi-sdk](https://github.com/equisoft-actions/generate-openapi-sdk)

Runs our OpenApi-SDK gradle tasks to generate and publish a SDK.
See https://github.com/kronostechnologies/standards/tree/master/gradle/openapi-sdk.

### [gradle-jacoco-check](https://github.com/equisoft-actions/gradle-jacoco-check)

Runs a gradle task expecting JaCoCo reports to be produced. The exported reports will follow naming conventions
detailed by our ADRs (https://confluence.equisoft.com/display/HRMI/ADR).

### [gradle-junit](https://github.com/equisoft-actions/gradle-junit)

Runs a gradle task expecting JUnit reports to be produced. The exported reports will follow naming conventions detailed
by our ADRs (https://confluence.equisoft.com/display/HRMI/ADR).

### [gradle-license-check](https://github.com/equisoft-actions/gradle-license-check)

Checks Gradle dependencies licenses on the project.
This action requires
the [global-conventions](https://github.com/kronostechnologies/standards/tree/master/gradle/global-conventions) plugin
to be installed.

### [gradle-sbom](https://github.com/equisoft-actions/gradle-sbom)

Utilizes CycloneDX to generate a SBOM. This SBOM will then be archived and uploaded to Dependency-Track.

## Go

### [golang-sast](https://github.com/equisoft-actions/golang-sast)

Runs GoKart to generate a SAST report of your codebase. Results are published to DefectDojo.

### [golang-sbom](https://github.com/equisoft-actions/golang-sbom)

Utilizes cyclonedx-gomod to generate a SBOM. This SBOM will then be archived and uploaded to Dependency-Track.

## PHP

### [composer](https://github.com/equisoft-actions/composer)

Install dependencies with composer (`composer install`)

### [composer-sbom](https://github.com/equisoft-actions/composer-sbom)

Utilizes cyclonedx-php-composer to generate a SBOM. This SBOM will then be archived and uploaded to Dependency-Track.

### [setup-php](https://github.com/equisoft-actions/setup-php)

Setup PHP with extensions.

### [phpcs](https://github.com/equisoft-actions/phpcs)

Lint PHP with PHP_CodeSniffer

### [phpunit](https://github.com/equisoft-actions/phpunit)

Runs PHPUnit and outputs a JUnit report, and a Clover report for coverage.

### [psalm](https://github.com/equisoft-actions/psalm)

Runs psalm

### [psalm-taint-analysis](https://github.com/equisoft-actions/psalm-taint-analysis)

Runs psalm with --taint-analysis and upload SARIF file artifact.

## Python

### [setup-python](https://github.com/equisoft-actions/setup-python)

Install Python dependencies with Pipenv.

### [pipenv-sbom](https://github.com/equisoft-actions/pipenv-sbom)

Utilizes cyclonedx-python to generate a SBOM. This SBOM will then be archived and uploaded to Dependency-Track.
Prerequisite: `pipenv install -d cyclonedx-bom`.

## NodeJS

### [nodejs-application-metadata](https://github.com/equisoft-actions/nodejs-application-metadata)

Resolves common application metadata like the application version or whether it is publishable (by our standards).

### [yarn-eslint](https://github.com/equisoft-actions/yarn-eslint)

Runs a yarn task expecting eslint reports to be produced. The exported reports will follow naming conventions
detailed by our ADRs (https://confluence.equisoft.com/display/HRMI/ADR).  
A report named `build/eslint/junit.xml` is expected under all circumstances.

### [yarn-install](https://github.com/equisoft-actions/yarn-install)

Install Yarn dependencies with Yarn. By default, the action will use a rolling cache key to prevent the cache size
from snowballing.

### [yarn-jest](https://github.com/equisoft-actions/yarn-jest)

Runs a yarn task expecting jest reports and coverage data to be produced. The reports will follow naming conventions
detailed by our ADRs (https://confluence.equisoft.com/display/HRMI/ADR).  
Report named `build/jest/junit.xml` with `build/jest/coverage/clover.xml` are expected under all circumstances.

### [yarn-mocha](https://github.com/equisoft-actions/yarn-mocha)

Runs a yarn task expecting mocha reports and coverage data to be produced. The reports will follow naming conventions
detailed by our ADRs (https://confluence.equisoft.com/display/HRMI/ADR).  
Report named `build/mocha/junit.xml` with `build/mocha/coverage/clover.xml` are expected under all circumstances.

### [yarn-npm-login](https://github.com/equisoft-actions/yarn-npm-login)

Login to any NPM Registry with yarn.

### [yarn-stylelint](https://github.com/equisoft-actions/yarn-stylelint)

Runs a yarn task expecting stylelint reports to be produced. The exported reports will follow naming conventions
detailed by our ADRs (https://confluence.equisoft.com/display/HRMI/ADR).  
A report named `build/stylelint/junit.xml` is expected under all circumstances.
