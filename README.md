Preview sample of Jenkins CIConnector

# Preparation

1. On SignPath.io
  * Create a CI User
  * Create a TBS
  * Create a Project `Executable` for a .exe file 
  * Link the TBS in the project
  * Add a signing policy `test-signing` with the CI user as submitter
  * Add a signing policy `rc-signing` with the CI user as submitter and approval process
2. Start a jenkins server with Powershell and PowerShell Module available

# Demo

1. Install the Jenkins CIConnector Plugin
2. Add `SignPath.TrustedBuildSystemToken` (Scope: System) and `SignPath.ExecutableProject.CIUserToken` (Scope: Global)
3. Create a new Pipeline `Sign Executable (test-signing)`
  * Add a parameter `ORGANIZATION_ID` with the org id as default
  * Select _Pipeline script from SCM_ and enter this repo URL and `Jenkinsfile.executable.test-signing` as name
4. Create a new Pipeline `Sign Executable (rc-signing)`
  * Add a parameter `ORGANIZATION_ID` with the org id as default
  * Select _Pipeline script from SCM_ and enter this repo URL and `Jenkinsfile.executable.release-signing` as name