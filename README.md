# Jira Exporter

The jupyter notebooks can be run in VS Code or Google Colab - and potentially any other jupyter engine (but these are the ones that I have tested in).

## Secrets

Secrets are stored need to be stored within a .env file with the following format

```text
SECRETS_HOST = "https://your-company.atlassian.net/"
SECRETS_USERNAME = "<you@your-company.com.au>"
SECRETS_PASSWORD = "ATATT........75"
```

For cloud based jira instances the username must be a email and the password is an api key. To generate an api key visit <https://id.atlassian.com/manage-profile/security/api-tokens>.

For server based jira the username is the login user name and the password is the login password.

If using Google Colab a prompt is presented to allow for a .env file to be uploaded,  saved and renamed to the correct file.

## Data Flows

The data flows were converted from power bi data flows and therefore share the name.

Data flows are the ingest point of data where initial table structure, column types, and column names are produced.

There is no modelling done within these data flows, e.g. no relationship checks are performed to ensure that primary keys are present and 1:Many relationships are validated (in order to create a star or snowflake model).
