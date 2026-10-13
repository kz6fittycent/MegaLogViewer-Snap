[![megalogviewer](https://snapcraft.io/megalogviewer/badge.svg)](https://snapcraft.io/megalogviewer)[![🧪 Snap Builds](https://github.com/kz6fittycent/MegaLogViewer-Snap/actions/workflows/test-snap-can-build.yml/badge.svg?branch=master)](https://github.com/kz6fittycent/MegaLogViewer-Snap/actions/workflows/test-snap-can-build.yml)[![📣 Call for Testing](https://github.com/kz6fittycent/MegaLogViewer-Snap/actions/workflows/call-for-testing.yml/badge.svg?branch=master)](https://github.com/kz6fittycent/MegaLogViewer-Snap/actions/workflows/call-for-testing.yml)


# MegaLogViewer MegaSquirt Edition

To install:
`sudo snap install megalogviewer`

After installing, run the following command:

`sudo snap connect megalogviewer:removable-media`

To run:

Click on the desktop icon or run it from your terminal: `megalogviewer`

Preferences are kept in `~/snap/megalogviewer/current/.efiAnalytics`. Your
`~/TunerStudioProjects` and `~/Documents` folders are available inside the app
as usual.

This is NOT an officially supported snap from EFI Analytics.

### Release process

New MegaLogViewer releases are picked up automatically. Once a day, the
[📣 Call for Testing](.github/workflows/call-for-testing.yml) workflow checks
the EFI Analytics download page. When there's a newer release than the one in
`latest/candidate`, or the packaging on `master` changes, it builds the snap,
uploads it to `latest/candidate` and opens a **Call for testing** issue with
screenshots from a clean VM.

To try a candidate build:

`sudo snap refresh megalogviewer --channel latest/candidate`

Maintainers release a tested revision to stable by commenting
`/promote <revision> stable done` on its issue
([🚀 Promote to Stable](.github/workflows/promote-to-stable.yml)).

## License

The packaging in this repository (snapcraft.yaml, scripts and workflows) is
released under the [MIT License](LICENSE). MegaLogViewer itself is
proprietary software from EFI Analytics and is not covered by this license;
the snap downloads it from efianalytics.com at build time.
