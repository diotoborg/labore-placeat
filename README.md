# @diotoborg/labore-placeat

[![Build Status](https://img.shields.io/github/actions/workflow/status/carloscuesta/@diotoborg/labore-placeat/ci.yml?branch=master&style=flat-square)](https://github.com/diotoborg/labore-placeat/actions?query=workflow%3ACI+branch%3Amaster)
[![Codecov](https://img.shields.io/codecov/c/github/carloscuesta/@diotoborg/labore-placeat.svg?style=flat-square)](https://codecov.io/gh/carloscuesta/@diotoborg/labore-placeat)
[![Npm Version](https://img.shields.io/npm/v/@diotoborg/labore-placeat.svg?style=flat-square)](https://www.npmjs.com/package/@diotoborg/labore-placeat)
[![Npm Downloads](https://img.shields.io/npm/dt/@diotoborg/labore-placeat.svg?style=flat-square)](https://www.npmjs.com/package/@diotoborg/labore-placeat)

> A simple and reusable React-Native [error boundary](https://react.dev/reference/react/Component#catching-rendering-errors-with-an-error-boundary) component 🐛

## Install

```bash
yarn add @diotoborg/labore-placeat
```

## Documentation

- [Installation](https://@diotoborg/labore-placeat.js.org/install)
- [Usage](https://@diotoborg/labore-placeat.js.org/usage/recovering-errors)
  - [Recovering Errors](https://@diotoborg/labore-placeat.js.org/usage/recovering-errors)
  - [Logging Errors](https://@diotoborg/labore-placeat.js.org/usage/logging-errors)
  - [Rendering a Fallback Component](https://@diotoborg/labore-placeat.js.org/usage/rendering-a-custom-fallback-ui)
- [API](https://@diotoborg/labore-placeat.js.org/api/errorboundary)
  - [`ErrorBoundary`](https://@diotoborg/labore-placeat.js.org/api/errorboundary)
  - [`FallbackComponent`](https://@diotoborg/labore-placeat.js.org/api/fallbackcomponent)
- [FAQ](https://@diotoborg/labore-placeat.js.org/faq)

## API

### [`ErrorBoundary`](https://@diotoborg/labore-placeat.js.org/api/errorboundary)

These are the props that you can pass to the `ErrorBoundary` component:

| Property            | Type              | Required | Default             |
|---------------------|-------------------|----------|---------------------|
| `Children`          | `React.Children`  | `true`   |                     |
| `FallbackComponent` | `React.Component` | `false`  | `FallbackComponent` |
| `onError`           | `Function`        | `false`  |                     |

#### `Children`

Any children that can throw an error. 

#### [`FallbackComponent`](https://@diotoborg/labore-placeat.js.org/api/fallbackcomponent)

The fallback component that will be rendered after catching an error.
By default the library comes with a built-in component.

#### `onError`

A function that receives two arguments:

- `error`: The error catched by the component.
- `stackTrace`: The stacktrace of the error.

```js
onError(error: Error, stackTrace: string): void
```

### [`FallbackComponent`](https://@diotoborg/labore-placeat.js.org/api/fallbackcomponent)

These are the props that the `FallbackComponent` receives:

| Property   | Type       | Default |
|------------|------------|---------|
| error      | `Error`    |         |
| resetError | `Function` |         |

#### `error`

The error object.

#### `resetError`

A function to reset the error state. You'll want to call this function to recover from the error state.

```js
resetError(): void
```

## Demo

<img
  src='https://user-images.githubusercontent.com/7629661/111866027-bc158e00-896a-11eb-8140-cfdc5d19527c.gif'
  alt='@diotoborg/labore-placeat'
  width='354px'
/>
