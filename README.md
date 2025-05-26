# maven-central-example

A reference project showcasing Maven Central publishing via Central Portal with Maven and GitHub Actions.

# Setup
Provision four GitHub Secrets in your repository:
- `MAVEN_CENTRAL_USERNAME`
- `MAVEN_CENTRAL_PASSWORD`
- `MAVEN_GPG_PRIVATE_KEY`
- `MAVEN_GPG_PASSPHRASE`

# Releasing

To release a new version, run `release:prepare` locally. 

This will prepare the project for release by updating the version number, commiting the changes, tagging the release, and pushing the changes to the remote repository.

Once you're ready to publish the release to Maven Central (think twice, this can't be undone), trigger the `release` GitHub Action.

Snapshots are automatically published on every push to the `main` branch.
