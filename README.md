# lcov-report-action-with-context

Add summary of coverage report as comment on Pull Request.

## Usage

No need to run if not triggered by pull_request

```yaml
    - name: Coverage Report on Pull Request with Additional Monorepo Context
      uses: Subatomic-Agency/lcov-report-action-with-context@0.1.3
      with:
        github-token: ${{ secrets.GITHUB_TOKEN }}
        package-name: monorepo-package-name
        coveralls-link: https://path.to.your.build
        lcov-path: coverage/lcov.info
        production-lcov-path: coverage/production.lcov.info
      if: github.event_name == 'pull_request'
```