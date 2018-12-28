# SMTP Relay

This is a helm chart for [posfix-relay-host](https://github.com/ullbergm/kubernetes-postfix-relay-host/).

## Installing

To install the chart:

```bash
helm install --name smtp-server ullbergm/smtp-server
```

## Uninstalling

To uninstall the chart:

```bash
helm delete --purge smtp-server
```

## Configuration

The following tables lists the configurable parameters of the Sentry chart and their default values.

| Parameter                         | Description                         | Default |
|-----------------------------------|-------------------------------------|---------|
| `image.repository`                | Image repository                    | `linuxserver/smtp-server` |
| `image.tag`                       | Image tag.                          | `154` |
| `image.pullPolicy`                | Image pull policy                   | `IfNotPresent` |
| `smtpRelayHost`                   | SMTP Relay host                     | `[email-smtp.us-east-1.amazonaws.com]:587` |
| `smtpRelayMyHostname`             | SMTP Relay server local hostname    | `{}` |
| `smtpRelayUsername`               | Upstream SMTP server username       | `{}` |
| `smtpRelayPassword`               | Upstream SMTP server password       | `{}` |
