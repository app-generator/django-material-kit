# Change Log

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
