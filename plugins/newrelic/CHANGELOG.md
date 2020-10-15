# @backstage/plugin-newrelic

## 0.2.0
### Minor Changes

- 28edd7d29: Create backend plugin through CLI
- 4512b9967: The New Relic plugin now uses the Backstage proxy to communicate with New Relic's API.
  
  Please update your `app-config.yaml` as follows:
  
  ```yaml
  # Old Config
  newrelic:
    api:
      baseUrl: 'https://api.newrelic.com/v2'
      key: NEW_RELIC_REST_API_KEY
  ```
  
  ```yaml
  # New Config
  proxy:
    '/newrelic/apm/api':
      target: https://api.newrelic.com/v2
      headers:
        X-Api-Key:
          $env: NEW_RELIC_REST_API_KEY
  ```

### Patch Changes

- Updated dependencies [819a70229]
- Updated dependencies [ae5983387]
- Updated dependencies [0d4459c08]
- Updated dependencies [482b6313d]
- Updated dependencies [1c60f716e]
- Updated dependencies [144c66d50]
- Updated dependencies [b79017fd3]
  - @backstage/core@0.2.0
  - @backstage/theme@0.2.0
