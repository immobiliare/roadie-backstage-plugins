# @roadiehq/backstage-plugin-prometheus

## 2.4.1

### Patch Changes

- 3a870726: Bump the `msw` dependency to `^1.0.1`

## 2.4.0

### Minor Changes

- 7c9fd336: Users can now add a callback to an `EntityPrometheusAlertCard` component. The component with callback can look like this:

  ```typescript
  <EntityPrometheusAlertCard onRowClick={callbackFunction} />
  ```

  And `callbackFunction` can have the following definition:

  ```typescript
  const callbackFunction = (arg: Alerts) => {
    ...
  };
  ```

  Where the `Alerts` type is a user-defined type to more easily parse JSON definition (`any` type can also be used). This callback is optional; if not supplied, tables in the row are not clickable.

  This change modifies `PrometheusAlertStatus`, which adds `onRowClick` event to a `Table` component.

## 2.3.0

### Minor Changes

- 87530639: Users can now define a new annotation, `prometheus.io/labels`. This annotation defines which labels will be included in the displayed table; if the annotation is not applied, the result is just filtered using `prometheus.io/alert` annotation. Example of usage:

  ```
  prometheus.io/labels: "label1=value1,label2=value2"
  ```

  This change modifies `useAlerts`, which adds filtering of alerts and adds a definition of new annotation. It also creates tests that verify this functionality.

## 2.2.3

### Patch Changes

- 6d186f0f: Bump plugin's version to backstage version 1.10.1

## 2.2.2

### Patch Changes

- 054d585b: Bump plugin versions to be compatible by backstage 1.9.1

## 2.2.1

### Patch Changes

- 7084d814: Bump plugins version to backstage 1.8.3

## 2.2.0

### Minor Changes

- 015aebdf: Bump plugins version to be compatible by backstage 1.7

## 2.1.3

### Patch Changes

- 073190b9: Update luxon to version 3.

## 2.1.2

### Patch Changes

- eaa0bb2: update dependencies

## 2.1.1

### Patch Changes

- 151b46b: bump to latest backstage package versions

## 2.1.0

### Minor Changes

- 5b305b9: Add ability to use multiple instances over proxy annotation.

## 2.0.3

### Patch Changes

- c9cfaad: Release all plugins after fixing typescript exports issue.

## 2.0.2

### Patch Changes

- 86eca6a: Update dependencies

## 2.0.1

### Patch Changes

- 6b4cc16: Update dependencies
  Add package information to the package.jsons, to tell the backstage cli how to run the tests

## 2.0.0

### Major Changes

- df841f0: Update dependecies to follow latest upstream version. Removed deprecated props of type 'Entity' passed into components as it is grabbed from context instead.

## 1.4.0

### Minor Changes

- f0421b4: Bumped to the latest upstream packages versions

## 1.3.11

### Patch Changes

- f5cd7e4: Update dependencies to latest Backstage packages

## 1.3.10

### Patch Changes

- 46b19a3: Update dependencies

## 1.3.9

### Patch Changes

- c779d9e: Update dependencies

## 1.3.8

### Patch Changes

- 7da7bfe: Update dependencies

## 1.3.7

### Patch Changes

- 5ae1b4b: Update README.md files

## 1.3.6

### Patch Changes

- b5db653: Update dependecies to latest packages

## 1.3.5

### Patch Changes

- a02dbf5: Migrating to TestApiProvider in the tests

## 1.3.4

### Patch Changes

- 142ce1c: Moved React dependencies to `peerDependencies` and allow both React v16 and v17 to be used.

## 1.3.3

### Patch Changes

- ecd06f5: Make "@backstage/core-app-api" a dev dependency

## 1.3.2

### Patch Changes

- 49abec7: Update patch to release new changes.

## 1.3.1

### Patch Changes

- a728fd1: Update underlying packages and release.

## 1.3.0

### Minor Changes

- ed90f25: Breaking dependency updates for @backstage/core-app-api, @backstage/test-utils, @backstage/core-plugin-api, @backstage/backend-common && @backstage/integration

## 1.2.3

### Patch Changes

- 120ca2e: Removed deprecated `description` option from `ApiRefConfig` for all plugins

## 1.2.2

### Patch Changes

- 4d426f9: Updated dependencies to follow latest Backstage release

## 1.2.1

### Patch Changes

- 3f280ef: Updated 'msw' package version in order to correctly run tests.
