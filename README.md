# Hugo Site Deployment to Firebase with GitHub Actions

This repository automates the deployment of a Hugo-based website to Firebase Hosting using GitHub Actions. Each push to the `main` branch triggers the workflow, ensuring the site is built with the latest **Hugo Extended** version and includes any configured Git submodules, such as themes.

## Features

- **Automated Deployment**: Publishes updates on every push to the `main` branch.
- **Latest Hugo Extended Version**: Always uses the most recent Hugo Extended release.
- **Firebase Hosting**: Deploys the site directly to Firebase.
- **Submodule Support**: Automatically includes Git submodules, ensuring the theme and other dependencies are integrated.

## Firebase Token Setup

To authorize deployments to Firebase, you need to generate a Firebase token:

1. Run `firebase login:ci` locally to generate the token.
2. Add the token to your GitHub repository as a secret:
   - Navigate to **Settings > Secrets and variables > Actions**.
   - Create a new secret named `FIREBASE_TOKEN` and paste the token.

This workflow handles the build and deploy steps, providing an efficient and reliable process for publishing your Hugo site.

## License

This project is licensed under the MIT License.