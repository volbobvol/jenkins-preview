Preview sample of Jenkins CIConnector

# Preparation

1. On SignPath.io
  * Create a CI User
  * Create a TBS
  * Create a Project `EXE` for a .exe file 
  * Link the TBS in the project
  * Add a signing policy `sync-signing` with the CI user as submitter
  * Add a signing policy `async-signing` with the CI user as submitter and approval process
2. Start a jenkins server with Powershell and PowerShell Module available

# Demo

1. Install the Jenkins CIConnector Plugin
2. Add `SignPath.TrustedBuildSystemToken` (Scope: System) and `SignPath.ProjectX.CIUserToken` (Scope: Global)
3. Create a new Pipeline `Sign Code (Sync)`
  * Add a parameter `ORGANIZATION_ID` with the org id as default
  * Select _Pipeline script from SCM_ and enter this repo URL and `Jenkinsfile.sync` as name
4. Create a new Pipeline `Sign Code (Async)`
  * Add a parameter `ORGANIZATION_ID` with the org id as default
  * Select _Pipeline script from SCM_ and enter this repo URL and `Jenkinsfile.async` as name