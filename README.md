# scm-bitbucket
[![Version][npm-image]][npm-url] ![Downloads][downloads-image] [![Build Status][status-image]][status-url] [![Open Issues][issues-image]][issues-url] [![Dependency Status][daviddm-image]][daviddm-url] ![License][license-image]

> This scm plugin extends the [scm-base-class](https://github.com/screwdriver-cd/scm-base), and provides methods to fetch and update data in Bitbucket.

## Usage

```bash
npm install screwdriver-scm-bitbucket
```

### Initialization

The class has a variety of knobs to tweak when interacting with Bitbucket.org.

| Parameter        | Type  |  Description |
| :-------------   | :---- | :-------------|
| config        | Object | Configuration Object |
| config.oauthClientId | String | OAuth Client ID provided by Bitbucket application |
| config.oauthClientSecret | String | OAuth Client Secret provided by Bitbucket application |
| config.https (false) | Boolean | Is the Screwdriver API running over HTTPS |
| config.fusebox ({}) | Object | [Circuit Breaker configuration][circuitbreaker] |
```js
const scm = new BitbucketScm({
    oauthClientId: 'your-client-id',
    oauthClientSecret: 'your-client-secret'
});
```

### Methods

For more information on the exposed methods please see the [scm-base-class].

## Testing

```bash
npm test
```

## License

Code licensed under the BSD 3-Clause license. See LICENSE file for terms.

[npm-image]: https://img.shields.io/npm/v/screwdriver-scm-bitbucket.svg
[npm-url]: https://npmjs.org/package/screwdriver-scm-bitbucket
[downloads-image]: https://img.shields.io/npm/dt/screwdriver-scm-bitbucket.svg
[license-image]: https://img.shields.io/npm/l/screwdriver-scm-bitbucket.svg
[issues-image]: https://img.shields.io/github/issues/screwdriver-cd/scm-bitbucket.svg
[issues-url]: https://github.com/screwdriver-cd/scm-bitbucket/issues
[status-image]: https://cd.screwdriver.cd/pipelines/2118d3886986f0bb831667abb4b36a20c52ed373/badge
[status-url]: https://cd.screwdriver.cd/pipelines/2118d3886986f0bb831667abb4b36a20c52ed373
[daviddm-image]: https://david-dm.org/screwdriver-cd/scm-bitbucket.svg?theme=shields.io
[daviddm-url]: https://david-dm.org/screwdriver-cd/scm-bitbucket
[scm-base-class]: https://github.com/screwdriver-cd/scm-base
