# Change Log

## [1.0.11] 2024-12-06
### Changes

- Bump UI Version

## [1.0.10] 2024-11-29
### Changes

> Update RM Links

- 👉 [Django Material Kit](https://app-generator.dev/product/material-kit/django/) - `Product Page`
- 👉 [Django Material Kit Documentation](https://app-generator.dev/docs/products/django/material-kit/index.html) - `Complete Information` and Support Links
  - [Getting Started with Django](https://app-generator.dev/docs/technologies/django/index.html) - a `comprehensive tutorial`
  - `Configuration`: Install Tailwind/Flowbite, Prepare Environment, Setting up the Database 
  - `Start with Docker`
  - `Manual Build`
  - `Start the project`
  - `Deploy on Render`

## [1.0.9] 2024-05-18
### Changes

- Updated DOCS (readme)
  - [Custom Development](https://appseed.us/custom-development/) Section
  - [CI/CD Assistance for AWS, DO](https://appseed.us/terms/#section-ci-cd)

## [1.0.8] 2024-03-05
### Changes

- Deprecate `distutils`
  - use `str2bool`
- Update Deps 
  - `requirements.txt` 
- Update [Custom Development](https://appseed.us/custom-development/) Section
  - New Pricing: `$3,999`

## [1.0.7] 2023-02-08
### Changes

- Bump UI: [Django Theme Material Kit](https://github.com/app-generator/django-theme-material-kit) `v1.0.18`
- DOCS Update (readme). New sections:
  - `How to customize the theme`
  - Render deployment
- Configure the project to use `home/templates`
- Added `custom-index` sample
- `Fix Docker` Execution
  - `Update Settings`: ALLOWED_HOSTS, CSRF_TRUSTED_ORIGINS `sections`

## [1.0.6] 2023-01-11
### Changes

- Bump Theme Version:
  - [Django Theme Material Kit](https://github.com/app-generator/django-theme-material-kit) `v1.0.16`

## [1.0.5] 2023-01-11
### Changes

- Move to theme-based pattern
  - [Django Theme Material Kit](https://github.com/app-generator/django-theme-material-kit)
- 🚀 `Deployment` 
  - `CI/CD` flow via `Render`

## [1.0.4] 2022-05-30
### Improvements

- Built with [Material Kit Generator](https://appseed.us/generator/material-kit/)  
  - Timestamp: `2022-05-31 07:49`

## [1.0.3] 2022-05-25
### Improvements

- Built with [Material Kit Generator](https://appseed.us/generator/material-kit/)  
  - Timestamp: `2022-05-25 22:04`
- Codebase refactoring
- Added CDN Support
  - via `.env` **ASSETS_ROOT** 

## [1.0.2] 2021-01-19
### Improvements

- Migrate all UI kit pages to Jinja

## [1.0.1] 2022-01-17
### Improvements

- Bump Django Codebase to [v2.0.0](https://github.com/app-generator/boilerplate-code-django/releases)
- Dependencies update (all packages) 
  - Django==4.0.1
- Settings update for Django 4.x
  - `New Parameter`: CSRF_TRUSTED_ORIGINS
    - [Origin header checking isn`t performed in older versions](https://docs.djangoproject.com/en/4.0/ref/settings/#csrf-trusted-origins)  

## [1.0.0] 2021-10-30 
### Initial Release

- Bump UI: Material Kit v3.0.0
  - Update Bootstrap to v5.1.1
  - Update to Material Design 2
- Codebase: [Django Boilerplate](https://github.com/app-generator/boilerplate-code-django) v1.0.6
  - Dependencies update (all packages) 
    - Django==3.2.6 (latest stable version)
  - Codebase:
    - Better Code formatting
    - Improved Files organization
    - Optimize imports
    - Docker Scripts Update
- Tooling: Added Gulp SCSS compilation scripts
