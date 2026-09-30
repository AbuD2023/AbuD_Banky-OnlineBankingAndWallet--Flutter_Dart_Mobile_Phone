# Contributing to AbuD Banky Mobile

Thank you for contributing to the Banky Flutter application. This repository contains the mobile client; the ASP.NET Core API is maintained separately at [AbuD Banky ASP.NET](https://github.com/AbuD2023/AbuD_Banky-OnlineBankingAndWallet--Razor-Pages-.NET-8-).

## Development setup

1. Fork and clone this repository.
2. Install Flutter and Dart versions compatible with `pubspec.yaml`, plus Android Studio or Xcode for your target platform.
3. Start a compatible `Banky.API` instance. Follow its [setup guide](https://github.com/AbuD2023/AbuD_Banky-OnlineBankingAndWallet--Razor-Pages-.NET-8-#quick-start).
4. Set the API base URL in `lib/core/api_constants.dart` to an address reachable from your emulator or device. Do not commit private network addresses or credentials.
5. Fetch dependencies and run the app:

   ```bash
   flutter pub get
   flutter run
   ```

## Before opening a pull request

- Format Dart code with `dart format lib test`.
- Run static analysis with `flutter analyze`.
- Run automated tests with `flutter test`.
- Add or update focused tests when changing behavior.
- Keep changes focused and consistent with existing Flutter, Provider, and RTL conventions.
- Update the README when setup instructions, API requirements, or user-visible capabilities change.

## API compatibility

The mobile app depends on the separately versioned `Banky.API`. If a change requires a new or modified API endpoint, document the required backend change and link to the corresponding issue or pull request. Do not silently assume that the API repository is updated in lockstep.

## Security and privacy

Never commit API secrets, tokens, real user data, identity documents, or production service addresses. Treat authentication, transfer, payment, and KYC changes as sensitive; explain the behavior and testing in the pull request. Report suspected vulnerabilities privately to the repository owner.

## Pull requests

Use a short descriptive branch name such as `feature/wallet-empty-state` or `fix/api-timeout`. In the pull request, summarize the user-facing change, list checks run, provide screenshots for visual changes where useful, and mention any API compatibility impact.

## License

By contributing, you agree that your contributions are made available under this repository's [MIT License](LICENSE).