Usage
---
Let's assume the following folder structure:

    - /myProject
    - /hasmobi-library

So both your project and this library located in the same folder. It's not really necessary, but works to illustrate this simple example.

Including the library inside your project requires 2 steps:

1. Include the library's `library` module and make it available inside your project. Edit the `settings.gradle` file in your project (`/myProject/settings.gradle`):

        include ':hasmobi-library'
        project(':hasmobi-library').projectDir = new File("../hasmobi-library/app")
2. Use the newly imported module inside any of your project's modules (e.g. the `app` module; `myproject/app/settings.gradle`):

        dependencies {
            ...
            compile project(':hasmobi-library')
        }