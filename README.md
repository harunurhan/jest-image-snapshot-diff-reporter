## jest-image-snapshot-diff-reporter

Reports diff images for failing image snapshot tests which are using [jest-image-snapshot](https://github.com/americanexpress/jest-image-snapshot). It helps to debug tests that are failing on CI where you can not access diff images directly. 

NOTE: Currently only prints them on console in base64 if `CI` env variable set

### Setup

```bash
yarn add --dev jest-image-snapshot-diff-reporter`
```


```json
"jest": {
  ...
  "reporters": ["default", "jest-image-snapshot-diff-reporter", ...]
  ...
}
```

### Roadmap

- Respect `jest-image-snapshot` configuration such as `customDiffDir` and `customSnapshotsDir`
- Support custom reporter function via config, that runs on each diff image. (so that they can be sent to somewhere else such as S3)
