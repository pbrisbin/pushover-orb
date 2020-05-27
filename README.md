# Pushover Orb [![CircleCI status](https://circleci.com/gh/pbrisbin/pushover-orb.svg "CircleCI status")](https://circleci.com/gh/pbrisbin/pushover-orb)

Built, test, and lint Stack-based Haskell projects in your CircleCI jobs.

## Usage

```yaml
version: 2.1

orbs:
  pushover: pbrisbin/pushover@x.y

workflows:
  commit:
    jobs:
      # ...

      - pushover/notify:
          name: notify
          title: '$CIRCLE_PROJECT_REPONAME'
          message: 'Released version ${CIRCLE_SHA1:0:10}'
          requires: release
```

See [all examples](./src/examples/).

---

[LICENSE](./LICENSE) | [CHANGELOG](./CHANGELOG.md)
