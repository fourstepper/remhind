# remhind

A notification daemon of events stored in directories

Those directories will be monitored for change in order to allow you to use
solution like [vdirsyncer](https://github.com/pimutils/vdirsyncer) to sync your
CalDAV server with your local filesystem.

## Getting Started

`remhind` use a [toml](https://github.com/toml-lang/toml) configuration file
indicating which directories holds your event files. Here's a simple example:

```
[calendars]
    [calendars.test]
    name = "Test"
    path = "~/projets/perso/remhind/test_calendar"
```

## Installing

`remhind` can be installed through PyPI using pip.

```
pip install remhind
```

## Running remhind as a systemd service

For running remhind as a service, you can use the example systemd service located at `contrib/remhind.service`.

`cp contrib/remhind.service ~/.config/systemd/user/remhind.service`

`systemctl enable --now remhind`

## Acknowledgments

This work has been inspired by the work of the [pimutils group](https://github.com/pimutils)
