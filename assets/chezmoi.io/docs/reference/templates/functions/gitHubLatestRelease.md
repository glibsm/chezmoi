# `gitHubLatestRelease` *user-repo*

`gitHubLatestRelease` calls the GitHub API to retrieve the latest release about
the given *user-repo*, returning structured data as defined by the [GitHub Go
API
bindings](https://pkg.go.dev/github.com/google/go-github/v41/github#RepositoryRelease).

Calls to `gitHubLatestRelease` are cached so calling `gitHubLatestRelease` with
the same *user-repo* will only result in one call to the GitHub API.

`gitHubLatestRelease` uses the same API request mechanism as `gitHubKeys`.

!!! example

    ```
    {{ (gitHubLatestRelease "docker/compose").TagName }}
    ```
