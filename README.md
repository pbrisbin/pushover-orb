**ARCHIVED**: For better or worse, I'm moving over to GitHub Actions for my CI needs and will not be maintaining
this package. Please see this fork, which picks up where I left off:

- https://github.com/masutaka/pushover-orb
- https://circleci.com/developer/orbs/orb/masutaka/pushover

# Pushover Orb [![CircleCI status](https://circleci.com/gh/pbrisbin/pushover-orb.svg "CircleCI status")](https://circleci.com/gh/pbrisbin/pushover-orb)

Send push notifications with [Pushover](https://pushover.net/).

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
          requires: [release]
```

See [all examples](./src/examples/).

---

[LICENSE](./LICENSE) | [CHANGELOG](./CHANGELOG.md)
