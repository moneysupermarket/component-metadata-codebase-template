# Repo Has Moved

This repo has moved to https://github.com/kronicle-tech/kronicle-metadata-codebase-template


# Component Metadata Template

This repo contains a template for adding a `component-metadata.yaml` file to a component's own codebase repo.

## Adding a `component-metadata.yaml` file to a component's own codebase repo

1. Copy the following files from this repo to your component's repo:

   | This Repo                                                            | Your Component's Repo            | Notes                                                                                                                  |
   |----------------------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------|
   | [gradle/component-metadata.gradle](gradle/component-metadata.gradle) | gradle/component-metadata.gradle | This will be a new file                                                                                                |
   | [build.gradle](build.gradle)                                         | build.gradle                     | Copy the `apply from:` line. You may also need to copy the other lines                                                 |
   | [component-metadata.yaml](component-metadata.yaml)                   | component-metadata.yaml          | This will be a new file                                                                                                |
   | [gradle.properties](gradle.properties)                               | gradle.properties                | Copy just the `componentMetadataVersion` line                                                                          |
   | [README-example.md](README-example.md)                               | README.md                        | Copy the contents into your existing file. Note the content needs copying from `README-example.md` and not `README.md` |

2. Replace the example YAML in the `component-metadata.yaml` file in your component's repo with YAML that describes the component(s) in that repo. The components in a repo can include multiple of a service or web app, a database, a queue etc. 
3. Run the following command in your codebase's repo to confirm your changes to the `component-metadata.yaml` file validate correctly:
   
   ```shell
   $ ./gradlew validateComponentMetadata
   ```

4. Raise a PR for your changes to your component's repo.
