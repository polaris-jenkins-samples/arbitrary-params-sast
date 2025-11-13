# Jenkins Execution Log

## Build Information
- **Job Name:** `MBP_Github_Polaris_Arbitrary_Sast_Scan/main`
- **Build Number:** #3
- **Build Status:** 🟢 **SUCCESS**
- **Duration:** 7 min 58 sec and counting
- **Timestamp:** 2025-11-13 15:45:21 UTC

---

## Console Output

```
Branch indexing
Connecting to https://api.github.com using madhusud@blackduck.com/****** (Github_Username_PAT)
Obtained nodejs-npm/Jenkinsfile from a45c3412d7391007989ddf655fc18ac2641e180b
Loading library blackduck-logs-publisher@main
Attempting to resolve main from remote references...
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git ls-remote -h -- https://github.com/integrations-garage/blackduck-logs-publisher # timeout=10
Found match: refs/heads/main revision e969196a63b1be83b84541b022f7aa52928bd5e5
The recommended git tool is: NONE
using credential Github_Username_PAT
 > git rev-parse --resolve-git-dir /Users/madhusud/.jenkins/workspace/Polaris_Arbitrary_Sast_Scan_main@libs/a0dda568bac7bbb4a171f59ba3f2660c21c69edc6356524e9ae8bb4500c12bbb/.git # timeout=10
Fetching changes from the remote Git repository
 > git config remote.origin.url https://github.com/integrations-garage/blackduck-logs-publisher # timeout=10
Fetching without tags
Fetching upstream changes from https://github.com/integrations-garage/blackduck-logs-publisher
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git fetch --no-tags --force --progress -- https://github.com/integrations-garage/blackduck-logs-publisher +refs/heads/*:refs/remotes/origin/* # timeout=10
Checking out Revision e969196a63b1be83b84541b022f7aa52928bd5e5 (main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f e969196a63b1be83b84541b022f7aa52928bd5e5 # timeout=10
Commit message: "Phase 3 - 2"
 > git rev-list --no-walk e969196a63b1be83b84541b022f7aa52928bd5e5 # timeout=10
[Pipeline] Start of Pipeline
[Pipeline] node
Running on mac-sh in /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Declarative: Checkout SCM)
[Pipeline] checkout
The recommended git tool is: NONE
using credential Github_Username_PAT
Fetching changes from the remote Git repository
Fetching without tags
 > git rev-parse --resolve-git-dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/.git # timeout=10
 > git config remote.origin.url https://github.com/polaris-jenkins-samples/arbitrary-params-sast.git # timeout=10
Fetching upstream changes from https://github.com/polaris-jenkins-samples/arbitrary-params-sast.git
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git fetch --no-tags --force --progress -- https://github.com/polaris-jenkins-samples/arbitrary-params-sast.git +refs/heads/main:refs/remotes/origin/main # timeout=10
Checking out Revision a45c3412d7391007989ddf655fc18ac2641e180b (main)
Commit message: "Delete jenkins-logs directory"
 > git config core.sparsecheckout # timeout=10
 > git checkout -f a45c3412d7391007989ddf655fc18ac2641e180b # timeout=10
 > git rev-list --no-walk 497dbd06a72ab7566c04271326768b1fa0b022d1 # timeout=10
[Pipeline] }
[Pipeline] // stage
[Pipeline] withEnv
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Build)
[Pipeline] script
[Pipeline] {
[Pipeline] echo
JOB_NAME: MBP_Github_Polaris_Arbitrary_Sast_Scan/main
[Pipeline] dir
Running in /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm
[Pipeline] {
[Pipeline] sh
+ node --version
v22.16.0
[Pipeline] sh
+ npm --version
10.9.2
[Pipeline] sh
+ npm install

up to date, audited 1480 packages in 20s

32 packages are looking for funding
  run `npm fund` for details

137 vulnerabilities (9 low, 35 moderate, 57 high, 36 critical)

To address issues that do not require attention, run:
  npm audit fix

To address all issues possible (including breaking changes), run:
  npm audit fix --force

Some issues need review, and may require choosing
a different dependency.

Run `npm audit` for details.
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // script
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (polaris-arbitrary-sast)
[Pipeline] script
[Pipeline] {
[Pipeline] dir
Running in /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm
[Pipeline] {
[Pipeline] security_scan
**************************** START EXECUTION OF BLACK DUCK SECURITY SCAN ****************************
[Security Scan] INFO: Jenkins Job name: MBP_Github_Polaris_Arbitrary_Sast_Scan
-------------------------------- Connection to node --------------------------------
[Security Scan] INFO: Jenkins job is running on agent node remotely
-------------------------- Parameter Validation Initiated --------------------------
[Security Scan] INFO:  --- product = [POLARIS]
[Security Scan] INFO: Parameters for polaris:
[Security Scan] INFO:  --- polaris_waitForScan = true
[Security Scan] INFO:  --- polaris_server_url = https://poc.polaris.blackduck.com
[Security Scan] INFO:  --- polaris_assessment_types = SAST,SCA
[Security Scan] INFO:  --- polaris_access_token = ******************************************************************************
[Security Scan] INFO:  --- coverity_clean_command = npm cache clean --force
[Security Scan] INFO:  --- coverity_build_command = npm install
------------------------------------------------------------------------------------
[Security Scan] INFO: Parameters for additional configuration:
[Security Scan] INFO:  --- network_airgap = false
[Security Scan] INFO: Polaris parameters are validated successfully
[Security Scan] INFO: Bridge download parameters are validated successfully
[Security Scan] INFO: Downloading Bridge CLI from: https://repo.blackduck.com/bds-integrations-release/com/blackduck/integration/bridge/binaries/bridge-cli-bundle/latest/bridge-cli-bundle-macos_arm.zip
[Security Scan] INFO: Bridge CLI successfully downloaded in: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle.zip
[Security Scan] INFO: Deleting previous Bridge CLI folder: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm
[Security Scan] INFO: Unzipping Bridge CLI zip file from: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle.zip
[Security Scan] INFO: Bridge CLI installed successfully in: /Users/madhusud/bridge-cli-bundle
------------------------------------------------------------------------------------
[Security Scan] INFO: Bridge CLI version is - 3.9.2
[Security Scan] INFO: Jenkins Job name: MBP_Github_Polaris_Arbitrary_Sast_Scan
[Security Scan] INFO: Polaris Application Name: arbitrary-params-sast
[Security Scan] INFO: Polaris Project Name: arbitrary-params-sast
[Security Scan] INFO: Polaris Branch Name: main
[Security Scan] INFO: Jenkins Job name: MBP_Github_Polaris_Arbitrary_Sast_Scan
[Security Scan] INFO: Executable command line arguments: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm/bridge-cli --stage polaris --input /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/polaris_input16865566606878877341.json --out .bridge/output/scan_info_out.json

******************************* START EXECUTION OF BRIDGE CLI *******************************
2025-11-13 15:38:28.4832 IST [Bridge CLI] INFO: Using cache directory: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm
2025-11-13 15:38:28.5032 IST [Bridge CLI] INFO: Found version "3.0.371" in registry for workflow "polaris", trying to load it from local cache
2025-11-13 15:38:29.9010 IST [Bridge CLI] INFO: Input Resources:
2025-11-13 15:38:29.9010 IST [Bridge CLI] INFO: resource = value [source]
2025-11-13 15:38:29.9011 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-13 15:38:29.9011 IST [Bridge CLI] INFO: coverity.build.command = npm install [polaris_input16865566606878877341.json]
2025-11-13 15:38:29.9011 IST [Bridge CLI] INFO: coverity.clean.command = npm cache clean --force [polaris_input16865566606878877341.json]
2025-11-13 15:38:29.9011 IST [Bridge CLI] INFO: network.airgap = false [polaris_input16865566606878877341.json]
2025-11-13 15:38:29.9011 IST [Bridge CLI] INFO: polaris.accesstoken = ***************************************** [polaris_input16865566606878877341.json]
2025-11-13 15:38:29.9011 IST [Bridge CLI] INFO: polaris.application.name = arbitrary-params-sast [polaris_input16865566606878877341.json]
2025-11-13 15:38:29.9011 IST [Bridge CLI] INFO: polaris.assessment.types = [SAST SCA] [polaris_input16865566606878877341.json]
2025-11-13 15:38:29.9011 IST [Bridge CLI] INFO: polaris.branch.name = main [polaris_input16865566606878877341.json]
2025-11-13 15:38:29.9011 IST [Bridge CLI] INFO: polaris.project.name = arbitrary-params-sast [polaris_input16865566606878877341.json]
2025-11-13 15:38:29.9011 IST [Bridge CLI] INFO: polaris.serverUrl = https://poc.polaris.blackduck.com [polaris_input16865566606878877341.json]
2025-11-13 15:38:29.9012 IST [Bridge CLI] INFO: polaris.waitForScan = true [polaris_input16865566606878877341.json]
2025-11-13 15:38:29.9012 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-13 15:38:29.9012 IST [Bridge CLI] INFO: Starting adapters for stage polaris
2025-11-13 15:38:29.9028 IST [Bridge CLI] INFO: Starting Adapter: Polaris Status Provider
2025-11-13 15:38:29.9030 IST [Bridge CLI] INFO: Starting Adapter: Polaris SCM Discovery
2025-11-13 15:38:29.9030 IST [Bridge CLI] INFO: Starting Adapter: Polaris Initializer
2025-11-13 15:38:29.9031 IST [Bridge CLI] INFO: Starting Adapter: Polaris Controller
2025-11-13 15:38:30.2942 IST [Polaris SCM Discovery] INFO: Adapter finished
2025-11-13 15:38:30.3001 IST [Bridge CLI] INFO: Starting Adapter: Set Polaris Assessment Mode to CI
2025-11-13 15:38:30.3003 IST [Set Polaris Assessment Mode to CI] INFO: Provided value for resource 'polaris.assessment.mode'
2025-11-13 15:38:30.3003 IST [Set Polaris Assessment Mode to CI] INFO: Adapter finished
2025-11-13 15:38:30.3058 IST [Bridge CLI] INFO: Starting Adapter: Create Polaris Project & Branch By Default
2025-11-13 15:38:30.3060 IST [Create Polaris Project & Branch By Default] INFO: Provided value for resource 'polaris.onboarding'
2025-11-13 15:38:30.3060 IST [Create Polaris Project & Branch By Default] INFO: Adapter finished
2025-11-13 15:38:33.3469 IST [Polaris Initializer] INFO: Successfully created test for "SCA(scaPackage)" assessment. The short test ID is "9CLEIK6"
2025-11-13 15:38:33.3489 IST [Polaris Initializer] INFO: Successfully created test for "SAST(sastFull)" assessment. The short test ID is "W0VSH85"
2025-11-13 15:38:33.3784 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.id'
2025-11-13 15:38:33.3787 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.id'
2025-11-13 15:38:33.3791 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.shortId'
2025-11-13 15:38:33.3794 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.shortId'
2025-11-13 15:38:33.3797 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.streamId'
2025-11-13 15:38:33.3800 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.project.id'
2025-11-13 15:38:33.3802 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.branch.id'
2025-11-13 15:38:33.3805 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.portfolioid'
2025-11-13 15:38:33.3807 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.tenant.id'
2025-11-13 15:38:33.3809 IST [Polaris Initializer] INFO: Provided value for resource 'polaris.application.id'
2025-11-13 15:38:33.3814 IST [Polaris Initializer] INFO: Adapter finished
2025-11-13 15:38:33.4000 IST [Bridge CLI] INFO: Starting Adapter: Check pull request
2025-11-13 15:38:33.7413 IST [Check pull request] INFO: Provided value for resource 'environment.scan.pull'
2025-11-13 15:38:33.7418 IST [Check pull request] INFO: Adapter finished
2025-11-13 15:38:34.0838 IST [Polaris Controller] INFO: Running for "sca" assessment with scan type "scaPackage"
2025-11-13 15:38:34.0895 IST [Polaris Controller] INFO: fetching recommended "detect" tool info...
2025-11-13 15:38:34.8319 IST [Polaris Controller] INFO: checking "detect" tool installation inside bridge home directory: /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/10.4.0
2025-11-13 15:38:34.8320 IST [Polaris Controller] INFO: Running command:/Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home/bin/java -version
2025-11-13 15:38:34.9171 IST [Polaris Controller] INFO: Checking tool version for "detect" in "/Users/madhusud/.blackduck/bridge/tools/blackduck-detect/10.4.0"
2025-11-13 15:38:34.9210 IST [Polaris Controller] INFO: Got tool version for "detect": 10.4.0
2025-11-13 15:38:35.2069 IST [Polaris Controller] INFO: "detect" tool is already installed...
2025-11-13 15:38:35.2070 IST [Polaris Controller] INFO: Running for "sast" assessment with scan type "sastFull"
2025-11-13 15:38:35.2070 IST [Polaris Controller] INFO: fetching recommended "coverity" tool info...
2025-11-13 15:38:35.5037 IST [Polaris Controller] INFO: checking "coverity" tool installation inside bridge home directory: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0
2025-11-13 15:38:35.5038 IST [Polaris Controller] INFO: Checking tool version for "cov_thin_client" in "/Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0"
2025-11-13 15:38:35.5045 IST [Polaris Controller] INFO: Running command:/Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/coverity --version
2025-11-13 15:38:35.5957 IST [Polaris Controller] INFO: Got tool version for "cov_thin_client": 2025.9.0
2025-11-13 15:38:35.8838 IST [Polaris Controller] INFO: "coverity" tool is already installed...
2025-11-13 15:38:35.8839 IST [Polaris Controller] INFO: fetching recommended "Sigma" tool info...
2025-11-13 15:38:36.1800 IST [Polaris Controller] INFO: checking "Sigma" tool installation inside bridge home directory: /Users/madhusud/.blackduck/bridge/tools/sigma/2025.10.0
2025-11-13 15:38:36.1801 IST [Polaris Controller] INFO: Checking tool version for "sigma" in "/Users/madhusud/.blackduck/bridge/tools/sigma/2025.10.0"
2025-11-13 15:38:36.1803 IST [Polaris Controller] INFO: Running command:/Users/madhusud/.blackduck/bridge/tools/sigma/2025.10.0/sigma --version
2025-11-13 15:38:36.5803 IST [Polaris Controller] INFO: Got tool version for "sigma": 2025.10.0
2025-11-13 15:38:36.8748 IST [Polaris Controller] INFO: "Sigma" tool is already installed...
2025-11-13 15:38:36.9062 IST [Polaris Controller] INFO: Provided value for resource 'coverity.id'
2025-11-13 15:38:36.9084 IST [Polaris Controller] INFO: Provided value for resource 'sigma.id'
2025-11-13 15:38:36.9087 IST [Polaris Controller] INFO: Provided value for resource 'detect.id'
2025-11-13 15:38:36.9089 IST [Bridge CLI] INFO: Starting adapters for stage polaris-sca-package
2025-11-13 15:38:36.9089 IST [Bridge CLI] INFO: Starting adapters for stage polaris-sast
2025-11-13 15:38:36.9089 IST [Bridge CLI] INFO: Starting adapters for stage polaris-artifacts-uploader
2025-11-13 15:38:36.9089 IST [Bridge CLI] INFO: Starting adapters for stage polaris-post-processing
2025-11-13 15:38:36.9124 IST [Bridge CLI] INFO: Starting Adapter: Polaris SCA Package Manager Scan
2025-11-13 15:38:36.9124 IST [Bridge CLI] INFO: Starting Adapter: Polaris Coverity Capture
2025-11-13 15:38:36.9124 IST [Bridge CLI] INFO: Starting Adapter: Polaris Artifacts Uploader
2025-11-13 15:38:36.9124 IST [Bridge CLI] INFO: Starting Adapter: Polaris Waiter
2025-11-13 15:38:36.9124 IST [Bridge CLI] INFO: Starting Adapter: Polaris Issues Fetcher
2025-11-13 15:38:36.9124 IST [Bridge CLI] INFO: Starting Adapter: Polaris Policy Checker
2025-11-13 15:38:36.9136 IST [Polaris Controller] INFO: Adapter finished
2025-11-13 15:38:36.9468 IST [Bridge CLI] INFO: Starting Adapter: Default Adapter for execution path
2025-11-13 15:38:36.9476 IST [Default Adapter for execution path] INFO: Provided value for resource 'coverity.execution.path'
2025-11-13 15:38:36.9477 IST [Default Adapter for execution path] INFO: Adapter finished
2025-11-13 15:38:36.9550 IST [Bridge CLI] INFO: Starting Adapter: Default Adapter for execution path
2025-11-13 15:38:36.9551 IST [Default Adapter for execution path] INFO: Provided value for resource 'sigma.execution.path'
2025-11-13 15:38:36.9552 IST [Default Adapter for execution path] INFO: Adapter finished
2025-11-13 15:38:37.3109 IST [Polaris Coverity Capture] INFO: Identified workflow: Polaris
2025-11-13 15:38:37.3121 IST [Polaris Coverity Capture] INFO: command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/coverity capture --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir -o capture.build.clean-command=npm cache clean --force -o analyze.location=connect -- npm install
2025-11-13 15:38:37.7191 IST [Polaris Coverity Capture] INFO: coverity 2025.9.0 covcli-2025.9-push-12
2025-11-13 15:38:37.7192 IST [Polaris Coverity Capture] INFO: envvar: COVERITY_CACHE_API_TOKEN_FILE=/var/folders/wm/gkd75sk54h57yqd0_j95gp2r0000gn/T/polaris_coverity_cache1702343118/.authKey
2025-11-13 15:38:37.7192 IST [Polaris Coverity Capture] INFO: envvar: COVERITY_CACHE_KEY=3a3b5550-c2d4-46ea-b662-2be4faebd74e
2025-11-13 15:38:37.7192 IST [Polaris Coverity Capture] INFO: envvar: COVERITY_CACHE_URL=https://poc.polaris.blackduck.com/api/cache
2025-11-13 15:38:37.7193 IST [Polaris Coverity Capture] INFO: envvar: COVERITY_CLI_CAPTURE_ZIP_ARCHIVE=/Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/idir.zip
2025-11-13 15:38:37.7193 IST [Polaris Coverity Capture] INFO: envvar: COVERITY_CLI_POLARIS_CLIENT=true
2025-11-13 15:38:37.7196 IST [Polaris Coverity Capture] INFO: Detected that stdout is not connected to a terminal.  Defaulting ticker mode to 'none'.
2025-11-13 15:38:37.7197 IST [Polaris Coverity Capture] INFO: If this is not correct, explicitly set the ticker mode to the desired value using the '--ticker-mode' option.
2025-11-13 15:38:37.7203 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-manage-emit --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir create
2025-11-13 15:38:37.7764 IST [Polaris Coverity Capture] INFO: Using lightweight capture with thin client.
2025-11-13 15:38:37.7766 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-internal-manage-cache check
2025-11-13 15:38:39.2133 IST [Polaris Coverity Capture] INFO: Caching is enabled.
2025-11-13 15:38:39.2155 IST [Polaris Coverity Capture] INFO: Telemetry is enabled
2025-11-13 15:38:40.2036 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-manage-emit --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir list-capture-diagnostics
2025-11-13 15:38:40.2175 IST [Polaris Coverity Capture] INFO: Executing action no-op: nothing to do for initialization
2025-11-13 15:38:40.6913 IST [Polaris Coverity Capture] INFO: Executing action Delete compiler configurations for intermediate directory '/Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir'
2025-11-13 15:38:40.6914 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --compiler gcc --comptype clangcc --template
2025-11-13 15:38:40.9956 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --compiler cc --comptype gcc --template
2025-11-13 15:38:41.2198 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --compiler c++ --comptype g++ --template
2025-11-13 15:38:41.4505 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --compiler clang --comptype clangcc --template
2025-11-13 15:38:41.6952 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --compiler java --comptype java --template
2025-11-13 15:38:41.9471 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --compiler go --comptype go --template
2025-11-13 15:38:42.1917 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --compiler ccache --comptype prefix --template
2025-11-13 15:38:42.4403 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --compiler kotlinc --comptype kotlinc --template
2025-11-13 15:38:42.6897 IST [Polaris Coverity Capture] WARNING: Template config template-java-config-0 already exists for java and will be reused. 
2025-11-13 15:38:42.6898 IST [Polaris Coverity Capture] WARNING: Template config template-apt-config-0 already exists for apt and will be reused. 
2025-11-13 15:38:42.6898 IST [Polaris Coverity Capture] WARNING: Template config template-javaw-config-0 already exists for javaw and will be reused. 
2025-11-13 15:38:42.6945 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/buildless-compiler-configs/coverity_config.xml --dart
2025-11-13 15:38:42.9503 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/buildless-compiler-configs/coverity_config.xml --javascript
2025-11-13 15:38:43.2022 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/buildless-compiler-configs/coverity_config.xml --php
2025-11-13 15:38:43.4564 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/buildless-compiler-configs/coverity_config.xml --python
2025-11-13 15:38:43.7050 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/buildless-compiler-configs/coverity_config.xml --ruby
2025-11-13 15:38:43.9524 IST [Polaris Coverity Capture] INFO: Executing action Configure build compiler: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-configure -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/buildless-compiler-configs/coverity_config.xml --comptype capture-config-files --file-regex $capture-config-files$ --template
2025-11-13 15:38:43.9761 IST [Polaris Coverity Capture] WARNING: Configuration already exists for file regex $capture-config-files$
2025-11-13 15:38:43.9762 IST [Polaris Coverity Capture] INFO:           and it will not be updated.
2025-11-13 15:38:44.4427 IST [Polaris Coverity Capture] INFO: Executing action no-op: no compilers need to be unconfigured
2025-11-13 15:38:44.8904 IST [Polaris Coverity Capture] INFO: Executing action no-op: compiler configurations loaded
2025-11-13 15:38:45.3898 IST [Polaris Coverity Capture] INFO: Executing action Execute clean command: sh -c npm cache clean --force
2025-11-13 15:38:45.6701 IST [Polaris Coverity Capture] INFO: npm warn using --force Recommended protections disabled.
2025-11-13 15:38:47.1368 IST [Polaris Coverity Capture] INFO: Executing action Invoke build capture: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-build --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/build-compiler-configs/coverity_config.xml --append-log --no-security-da --record-with-source --no-xrefs --enable-scan-transparency-data --bytecode-caching --force npm install
2025-11-13 15:38:47.6466 IST [Polaris Coverity Capture] INFO: Coverity Build Capture (64-bit) version 2025.9.0 on Darwin 24.6.0 arm64
2025-11-13 15:38:47.6467 IST [Polaris Coverity Capture] INFO: Internal version numbers: 477d3c5ddd p-2025.9-push-57
2025-11-13 15:38:47.6467 IST [Polaris Coverity Capture] INFO: 
2025-11-13 15:38:47.6554 IST [Polaris Coverity Capture] INFO: 
2025-11-13 15:39:44.0354 IST [Polaris Coverity Capture] INFO: npm warn deprecated urix@0.1.0: Please see https://github.com/lydell/urix#deprecated
2025-11-13 15:39:44.0359 IST [Polaris Coverity Capture] INFO: npm warn deprecated resolve-url@0.2.1: https://github.com/lydell/resolve-url#deprecated
2025-11-13 15:39:44.5302 IST [Polaris Coverity Capture] INFO: npm warn deprecated source-map-resolve@0.5.3: See https://github.com/lydell/source-map-resolve#deprecated
2025-11-13 15:39:44.7118 IST [Polaris Coverity Capture] INFO: npm warn deprecated source-map-url@0.4.1: See https://github.com/lydell/source-map-url#deprecated
2025-11-13 15:39:46.0188 IST [Polaris Coverity Capture] INFO: npm warn deprecated stable@0.1.8: Modern JS already guarantees Array#sort() is a stable sort, so this library is deprecated. See the compatibility table on MDN: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort#browser_compatibility
2025-11-13 15:39:46.2956 IST [Polaris Coverity Capture] INFO: npm warn deprecated try-resolve@1.0.1: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
2025-11-13 15:39:46.4392 IST [Polaris Coverity Capture] INFO: npm warn deprecated babel-plugin-remove-debugger@1.0.1: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
2025-11-13 15:39:46.5272 IST [Polaris Coverity Capture] INFO: npm warn deprecated babel-plugin-inline-environment-variables@1.0.1: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
2025-11-13 15:39:46.5274 IST [Polaris Coverity Capture] INFO: npm warn deprecated babel-plugin-runtime@1.0.7: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
2025-11-13 15:39:46.5279 IST [Polaris Coverity Capture] INFO: npm warn deprecated babel-plugin-react-constant-elements@1.0.3: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
2025-11-13 15:39:46.5282 IST [Polaris Coverity Capture] INFO: npm warn deprecated babel-plugin-undefined-to-void@1.1.6: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
2025-11-13 15:39:46.5287 IST [Polaris Coverity Capture] INFO: npm warn deprecated babel-plugin-member-expression-literals@1.0.1: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
2025-11-13 15:39:46.5289 IST [Polaris Coverity Capture] INFO: npm warn deprecated babel-plugin-react-display-name@1.0.3: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
2025-11-13 15:39:46.5290 IST [Polaris Coverity Capture] INFO: npm warn deprecated babel-plugin-remove-console@1.0.1: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
2025-11-13 15:39:46.5292 IST [Polaris Coverity Capture] INFO: npm warn deprecated babel-plugin-proto-to-assign@1.0.4: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
2025-11-13 15:39:46.5565 IST [Polaris Coverity Capture] INFO: npm warn deprecated babel-plugin-jscript@1.0.4: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
2025-11-13 15:39:46.6505 IST [Polaris Coverity Capture] INFO: npm warn deprecated babel-plugin-eval@1.0.1: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
2025-11-13 15:39:46.6648 IST [Polaris Coverity Capture] INFO: npm warn deprecated babel-plugin-property-literals@1.0.1: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
2025-11-13 15:39:46.6931 IST [Polaris Coverity Capture] INFO: npm warn deprecated babel-plugin-constant-folding@1.0.1: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
2025-11-13 15:39:46.8289 IST [Polaris Coverity Capture] INFO: npm warn deprecated babel-plugin-dead-code-elimination@1.0.2: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
2025-11-13 15:39:47.8185 IST [Polaris Coverity Capture] INFO: npm warn deprecated q@0.8.12: You or someone you depend on is using Q, the JavaScript Promise library that gave JavaScript developers strong feelings about promises. They can almost certainly migrate to the native JavaScript promise now. Thank you literally everyone for joining me in this bet against the odds. Be excellent to each other.
2025-11-13 15:39:47.8185 IST [Polaris Coverity Capture] INFO: npm warn deprecated
2025-11-13 15:39:47.8186 IST [Polaris Coverity Capture] INFO: npm warn deprecated (For a CapTP with native promises, see @endo/eventual-send and @endo/captp)
2025-11-13 15:39:48.5917 IST [Polaris Coverity Capture] INFO: npm warn deprecated json3@3.3.2: Please use the native JSON object instead of JSON 3
2025-11-13 15:39:49.5377 IST [Polaris Coverity Capture] INFO: npm warn deprecated transformers@2.1.0: Deprecated, use jstransformer
2025-11-13 15:39:49.5603 IST [Polaris Coverity Capture] INFO: npm warn deprecated constantinople@3.0.2: Please update to at least constantinople 3.1.1
2025-11-13 15:39:50.4879 IST [Polaris Coverity Capture] INFO: npm warn deprecated rimraf@2.6.3: Rimraf versions prior to v4 are no longer supported
2025-11-13 15:39:50.5079 IST [Polaris Coverity Capture] INFO: npm warn deprecated circular-json@0.3.3: CircularJSON is in maintenance only, flatted is its successor.
2025-11-13 15:39:50.5273 IST [Polaris Coverity Capture] INFO: npm warn deprecated inflight@1.0.6: This module is not supported, and leaks memory. Do not use it. Check out lru-cache if you want a good and tested way to coalesce async requests by a key value, which is much more comprehensive and powerful.
2025-11-13 15:39:51.2615 IST [Polaris Coverity Capture] INFO: npm warn deprecated glob@7.2.3: Glob versions prior to v9 are no longer supported
2025-11-13 15:39:51.2749 IST [Polaris Coverity Capture] INFO: npm warn deprecated coffee-script@1.12.7: CoffeeScript on NPM has moved to "coffeescript" (no hyphen)
2025-11-13 15:39:51.7302 IST [Polaris Coverity Capture] INFO: npm warn deprecated core-js@2.6.12: core-js@<3.23.3 is no longer maintained and not recommended for usage due to the number of issues. Because of the V8 engine whims, feature detection in old core-js versions could cause a slowdown up to 100x even if nothing is polyfilled. Some versions have web compatibility issues. Please, upgrade your dependencies to the actual version of core-js.
2025-11-13 15:39:52.3945 IST [Polaris Coverity Capture] INFO: npm warn deprecated swig@1.4.2: This package is no longer maintained
2025-11-13 15:39:52.6275 IST [Polaris Coverity Capture] INFO: npm warn deprecated jade@1.11.0: Jade has been renamed to pug, please install the latest version of pug instead of jade
2025-11-13 15:39:52.9849 IST [Polaris Coverity Capture] INFO: npm warn deprecated eslint@3.19.0: This version is no longer supported. Please see https://eslint.org/version-support for other options.
2025-11-13 15:39:54.0445 IST [Polaris Coverity Capture] INFO: npm warn deprecated glob@5.0.15: Glob versions prior to v9 are no longer supported
2025-11-13 15:39:54.0501 IST [Polaris Coverity Capture] INFO: npm warn deprecated q@1.5.1: You or someone you depend on is using Q, the JavaScript Promise library that gave JavaScript developers strong feelings about promises. They can almost certainly migrate to the native JavaScript promise now. Thank you literally everyone for joining me in this bet against the odds. Be excellent to each other.
2025-11-13 15:39:54.0501 IST [Polaris Coverity Capture] INFO: npm warn deprecated
2025-11-13 15:39:54.0502 IST [Polaris Coverity Capture] INFO: npm warn deprecated (For a CapTP with native promises, see @endo/eventual-send and @endo/captp)
2025-11-13 15:39:54.3383 IST [Polaris Coverity Capture] INFO: npm warn deprecated core-js@1.2.7: core-js@<3.23.3 is no longer maintained and not recommended for usage due to the number of issues. Because of the V8 engine whims, feature detection in old core-js versions could cause a slowdown up to 100x even if nothing is polyfilled. Some versions have web compatibility issues. Please, upgrade your dependencies to the actual version of core-js.
2025-11-13 15:39:54.5147 IST [Polaris Coverity Capture] INFO: npm warn deprecated q@1.5.1: You or someone you depend on is using Q, the JavaScript Promise library that gave JavaScript developers strong feelings about promises. They can almost certainly migrate to the native JavaScript promise now. Thank you literally everyone for joining me in this bet against the odds. Be excellent to each other.
2025-11-13 15:39:54.5148 IST [Polaris Coverity Capture] INFO: npm warn deprecated
2025-11-13 15:39:54.5148 IST [Polaris Coverity Capture] INFO: npm warn deprecated (For a CapTP with native promises, see @endo/eventual-send and @endo/captp)
2025-11-13 15:39:54.7307 IST [Polaris Coverity Capture] INFO: npm warn deprecated minimatch@0.3.0: Please update to minimatch 3.0.2 or higher to avoid a RegExp DoS issue
2025-11-13 15:39:54.8521 IST [Polaris Coverity Capture] INFO: npm warn deprecated glob@3.2.11: Glob versions prior to v9 are no longer supported
2025-11-13 15:39:55.4492 IST [Polaris Coverity Capture] INFO: npm warn deprecated core-js@1.2.7: core-js@<3.23.3 is no longer maintained and not recommended for usage due to the number of issues. Because of the V8 engine whims, feature detection in old core-js versions could cause a slowdown up to 100x even if nothing is polyfilled. Some versions have web compatibility issues. Please, upgrade your dependencies to the actual version of core-js.
2025-11-13 15:39:55.5084 IST [Polaris Coverity Capture] INFO: npm warn deprecated mkdirp@0.5.1: Legacy versions of mkdirp are no longer supported. Please update to mkdirp 1.x. (Note that the API surface has changed to use Promises in 1.x.)
2025-11-13 15:39:55.5985 IST [Polaris Coverity Capture] INFO: npm warn deprecated glob@7.1.1: Glob versions prior to v9 are no longer supported
2025-11-13 15:39:55.9214 IST [Polaris Coverity Capture] INFO: npm warn deprecated mkdirp@0.3.0: Legacy versions of mkdirp are no longer supported. Please update to mkdirp 1.x. (Note that the API surface has changed to use Promises in 1.x.)
2025-11-13 15:39:56.3479 IST [Polaris Coverity Capture] INFO: npm warn deprecated fsevents@1.2.13: Upgrade to fsevents v2 to mitigate potential security issues
2025-11-13 15:39:56.4199 IST [Polaris Coverity Capture] INFO: npm warn deprecated minimatch@2.0.10: Please update to minimatch 3.0.2 or higher to avoid a RegExp DoS issue
2025-11-13 15:39:56.7818 IST [Polaris Coverity Capture] INFO: npm warn deprecated core-js@1.2.7: core-js@<3.23.3 is no longer maintained and not recommended for usage due to the number of issues. Because of the V8 engine whims, feature detection in old core-js versions could cause a slowdown up to 100x even if nothing is polyfilled. Some versions have web compatibility issues. Please, upgrade your dependencies to the actual version of core-js.
2025-11-13 15:41:30.0243 IST [Polaris Coverity Capture] INFO: 
2025-11-13 15:41:30.0243 IST [Polaris Coverity Capture] INFO: added 737 packages, and audited 738 packages in 3m
2025-11-13 15:41:30.0244 IST [Polaris Coverity Capture] INFO: 
2025-11-13 15:41:30.0244 IST [Polaris Coverity Capture] INFO: 25 packages are looking for funding
2025-11-13 15:41:30.0244 IST [Polaris Coverity Capture] INFO:   run `npm fund` for details
2025-11-13 15:41:30.0638 IST [Polaris Coverity Capture] INFO: 
2025-11-13 15:41:30.0639 IST [Polaris Coverity Capture] INFO: 49 vulnerabilities (1 low, 10 moderate, 19 high, 19 critical)
2025-11-13 15:41:30.0639 IST [Polaris Coverity Capture] INFO: 
2025-11-13 15:41:30.0639 IST [Polaris Coverity Capture] INFO: To address issues that do not require attention, run:
2025-11-13 15:41:30.0639 IST [Polaris Coverity Capture] INFO:   npm audit fix
2025-11-13 15:41:30.0639 IST [Polaris Coverity Capture] INFO: 
2025-11-13 15:41:30.0639 IST [Polaris Coverity Capture] INFO: To address all issues possible (including breaking changes), run:
2025-11-13 15:41:30.0639 IST [Polaris Coverity Capture] INFO:   npm audit fix --force
2025-11-13 15:41:30.0639 IST [Polaris Coverity Capture] INFO: 
2025-11-13 15:41:30.0640 IST [Polaris Coverity Capture] INFO: Some issues need review, and may require choosing
2025-11-13 15:41:30.0640 IST [Polaris Coverity Capture] INFO: a different dependency.
2025-11-13 15:41:30.0640 IST [Polaris Coverity Capture] INFO: 
2025-11-13 15:41:30.0640 IST [Polaris Coverity Capture] INFO: Run `npm audit` for details.
2025-11-13 15:41:30.3243 IST [Polaris Coverity Capture] INFO: Attempting to detect unconfigured compilers in build
2025-11-13 15:41:30.3296 IST [Polaris Coverity Capture] INFO: |0----------25-----------50----------75---------100|
2025-11-13 15:41:30.4411 IST [Polaris Coverity Capture] INFO: ****************************************************
2025-11-13 15:41:30.4671 IST [Polaris Coverity Capture] WARNING: Recorded 0 C/C++ compilation units (0%) successfully. These compilation units are ready for replay
2025-11-13 15:41:30.4671 IST [Polaris Coverity Capture] WARNING: Recoverable errors were encountered during 1 of these C/C++ compilation units.
2025-11-13 15:41:30.4671 IST [Polaris Coverity Capture] INFO: 
2025-11-13 15:41:30.4671 IST [Polaris Coverity Capture] INFO:  For more details, please look at: 
2025-11-13 15:41:30.4671 IST [Polaris Coverity Capture] INFO:     /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/build-log.txt
2025-11-13 15:41:30.5339 IST [Polaris Coverity Capture] INFO: Executing action Collect Build Metrics
2025-11-13 15:41:30.5341 IST [Polaris Coverity Capture] INFO: Executing action Invalidate capture results
2025-11-13 15:41:30.5342 IST [Polaris Coverity Capture] INFO: Executing action Update uncaptured file timestamps for project "/Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/node_modules/consolidate/Makefile"
2025-11-13 15:41:30.5344 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-manage-emit --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir list-capture-diagnostics
2025-11-13 15:41:31.8178 IST [Polaris Coverity Capture] INFO: Executing action Emit files using buildless capture: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-internal-capture-files --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir -c /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/buildless-compiler-configs/coverity_config.xml --ticker-mode none --append-log --capture-list-file /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/capture-file-list-2764770943 --record-with-source
2025-11-13 15:41:31.8599 IST [Polaris Coverity Capture] INFO: Buildless capture started.
2025-11-13 15:41:31.8766 IST [Polaris Coverity Capture] INFO: Emitting 84 Files.
2025-11-13 15:41:32.3268 IST [Polaris Coverity Capture] INFO: Buildless capture completed.
2025-11-13 15:41:32.3286 IST [Polaris Coverity Capture] INFO: Executing action Delete unwanted TUs: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-manage-emit @@/Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir/coverity-cli/delete-unwanted-tus-action-3462883689
2025-11-13 15:41:32.3463 IST [Polaris Coverity Capture] INFO: Executing action Action cleanup: Unwanted TUs action cleanup
2025-11-13 15:41:32.3466 IST [Polaris Coverity Capture] INFO: Executing action deleteResidualTUs /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir
2025-11-13 15:41:32.3467 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-manage-emit --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir list-capture-diagnostics
2025-11-13 15:41:32.3627 IST [Polaris Coverity Capture] INFO: Executing action Invalidate capture results
2025-11-13 15:41:32.3627 IST [Polaris Coverity Capture] INFO: Executing action Invoke cov-run-sigma: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-run-sigma --project-dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir --coverity-config /var/folders/wm/gkd75sk54h57yqd0_j95gp2r0000gn/T/cov-run-sigma-config-2823231638/coverity.yaml --sigma-binary-path /Users/madhusud/.blackduck/bridge/tools/sigma/2025.10.0/sigma --enable-telemetry
2025-11-13 15:41:32.4020 IST [Polaris Coverity Capture] INFO: cov-run-sigma version 2025.9.0 on Darwin 24.6.0 arm64
2025-11-13 15:41:32.4020 IST [Polaris Coverity Capture] INFO: Internal version numbers: 477d3c5ddd p-2025.9-push-57
2025-11-13 15:41:32.4020 IST [Polaris Coverity Capture] INFO: 
2025-11-13 15:41:34.1929 IST [Polaris Coverity Capture] INFO: Executing action Action cleanup: Coverity configuration for Sigma
2025-11-13 15:41:35.1413 IST [Polaris Coverity Capture] INFO: Executing command: /Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/cov-manage-emit --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir list-capture-diagnostics
2025-11-13 15:41:35.2332 IST [Polaris Coverity Capture] INFO: Capture summary:
2025-11-13 15:41:35.2333 IST [Polaris Coverity Capture] INFO:     SUCCEEDED: 87
2025-11-13 15:41:35.2333 IST [Polaris Coverity Capture] INFO:     INCOMPLETE: 0
2025-11-13 15:41:35.2333 IST [Polaris Coverity Capture] INFO:     FAILED: 0
2025-11-13 15:41:35.2333 IST [Polaris Coverity Capture] INFO:     IGNORED: 3
2025-11-13 15:41:35.2333 IST [Polaris Coverity Capture] INFO:     FILES CAPTURED: 87
2025-11-13 15:41:35.2334 IST [Polaris Coverity Capture] INFO:     LINES OF CODE: 32921
2025-11-13 15:41:35.2361 IST [Polaris Coverity Capture] INFO: Capture phase took 2m56.027s.
2025-11-13 15:41:35.2361 IST [Polaris Coverity Capture] WARNING: !! SOURCES FOR UNSUPPORTED LANGUAGES WERE DETECTED !!
2025-11-13 15:41:35.2361 IST [Polaris Coverity Capture] WARNING: 
2025-11-13 15:41:35.2361 IST [Polaris Coverity Capture] WARNING: Source files for the following languages were detected, but these languages are not supported on Mac OS ARM:
2025-11-13 15:41:35.2361 IST [Polaris Coverity Capture] WARNING:   * C#
2025-11-13 15:41:35.2362 IST [Polaris Coverity Capture] WARNING: In order to analyze these files, please analyze the project on an operating system and architecture where they are supported.
2025-11-13 15:41:35.3047 IST [Polaris Coverity Capture] INFO: To analyze your project, type '/Users/madhusud/.blackduck/bridge/tools/cov-thin-client/2025.9.0/bin/coverity analyze --dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/2025.9.0/idir -o analyze.location=connect'.
2025-11-13 15:41:35.3069 IST [Polaris Coverity Capture] INFO: Coverity Capture completed successfully
2025-11-13 15:41:35.3134 IST [Polaris Coverity Capture] INFO: Provided value for resource 'coverity.completed'
2025-11-13 15:41:35.3136 IST [Polaris Coverity Capture] INFO: Provided value for resource 'coverity.idir.output'
2025-11-13 15:41:35.3137 IST [Polaris Coverity Capture] INFO: Provided value for resource 'polaris.test.sast.tests.sastFull.artifacts.path'
2025-11-13 15:41:35.3139 IST [Polaris Coverity Capture] INFO: Adapter finished
2025-11-13 15:41:35.3155 IST [Bridge CLI] INFO: Starting Adapter: Default Adapter for execution path
2025-11-13 15:41:35.3158 IST [Default Adapter for execution path] INFO: Provided value for resource 'detect.execution.path'
2025-11-13 15:41:35.3160 IST [Default Adapter for execution path] INFO: Adapter finished
2025-11-13 15:41:35.6578 IST [Polaris SCA Package Manager Scan] INFO: Running command /Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home/bin/java -jar /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/10.4.0/detect-10.4.0.jar --detect.cleanup=false --detect.bdio.file.name=scan --detect.bdio.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/bdio/blackduck_artifact --detect.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect --detect.tools=DETECTOR --detect.component.location.analysis.enabled=true --blackduck.offline.mode=true --blackduck.offline.mode.force.bdio=true
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] WARNING: --- Detect-Self-Updater:  Self-Update feature is disabled because of the following reasons:
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] WARNING: --- Detect-Self-Updater:  Detect in offline mode is incompatible with the Self-Update feature.
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] WARNING: --- Detect-Self-Updater:  Black Duck URL is required for the Self-Update feature.
2025-11-13 15:41:36.7231 IST [Polaris SCA Package Manager Scan] INFO: ______     _            _
2025-11-13 15:41:36.7232 IST [Polaris SCA Package Manager Scan] INFO: |  _  \   | |          | |
2025-11-13 15:41:36.7232 IST [Polaris SCA Package Manager Scan] INFO: | | | |___| |_ ___  ___| |_
2025-11-13 15:41:36.7232 IST [Polaris SCA Package Manager Scan] INFO: | | | / _ \ __/ _ \/ __| __|
2025-11-13 15:41:36.7232 IST [Polaris SCA Package Manager Scan] INFO: | |/ /  __/ ||  __/ (__| |_
2025-11-13 15:41:36.7232 IST [Polaris SCA Package Manager Scan] INFO: |___/ \___|\__\___|\___|\__|
2025-11-13 15:41:36.7233 IST [Polaris SCA Package Manager Scan] INFO: 
2025-11-13 15:41:36.8563 IST [Polaris SCA Package Manager Scan] INFO: 
2025-11-13 15:41:36.8563 IST [Polaris SCA Package Manager Scan] INFO: Detect Version: 10.4.0
2025-11-13 15:41:36.8563 IST [Polaris SCA Package Manager Scan] INFO: 
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Current property values:
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- --property = value [notes]
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ------------------------------------------------------------
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- blackduck.offline.mode = true [cmd] 
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- blackduck.offline.mode.force.bdio = true [cmd] 
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.bdio.file.name = scan [cmd] 
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.bdio.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/bdio/blackduck_artifact [cmd] 
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.cleanup = false [cmd] 
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.component.location.analysis.enabled = true [cmd] 
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.excluded.directories = /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge [env] 
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect [cmd] 
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- detect.tools = DETECTOR [cmd] 
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ------------------------------------------------------------
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Detect build date: 2025-04-24
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Source directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Output directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Run directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/runs/2025-11-13-10-11-36-818
2025-11-13 15:41:36.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] WARNING: --- Correlated Scanning is not available for Rapid/Stateless scan mode or offline scanning. A correlation ID will not be set.
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Docker tool will not be run.
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Bazel tool will not be run.
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Will include the Detectors tool.
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Searching for detectors.
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Evaluating detectors. This may take a while.
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ======================================================================================================
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Detector Report
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ======================================================================================================
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 	/Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm (depth 0)
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 		NPM Package Lock: SUCCESS
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 			Found file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/package-lock.json
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 			Found file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/package.json
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Detectors actions finished.
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Project name: owasp-nodejs-goat
2025-11-13 15:41:37.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Project version: 1.3.0
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Signature Scanner tool will not be run.
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Vulnerability Impact Analysis tool will not be run.
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- IaC Scanner tool will not be run.
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ##################################################################################################
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #                                                                                                #
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  Product Notice                                                                                #
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  © 2024 Black Duck Software, Inc.                                                              #
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  This Black Duck Component Locator and all associated documentation are proprietary            #
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  to Black Duck Software, Inc. and may only be used pursuant to the terms and conditions of a   #
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  written license agreement with Black Duck Software, Inc. All other use, reproduction,         #
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  modification, or distribution of the Black Duck Component Locator or the associated           #
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #  documentation is strictly prohibited.                                                         #
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- #                                                                                                #
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ##################################################################################################
2025-11-13 15:41:39.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Running Component Locator v1.1.12 on /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Component Location Analysis file saved at: /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/runs/2025-11-13-10-11-36-818/scan/components-with-locations.json
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ----------------------------------
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Creating status file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/runs/2025-11-13-10-11-36-818/status/status.json
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Skipping cleanup, it is disabled.
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ======== Detect Result ========
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Component Location Analysis File: /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/detect/runs/2025-11-13-10-11-36-818/scan/components-with-locations.json
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ======== Detect Status ========
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- NPM: SUCCESS
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Overall Status: SUCCESS - Detect exited successfully.
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- ===============================
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- 
2025-11-13 15:42:44.0000 IST [Polaris SCA Package Manager Scan][main] INFO: --- Detect duration: 00h 01m 08s 614ms
2025-11-13 15:42:44.6682 IST [Polaris SCA Package Manager Scan] INFO: Provided value for resource 'detect.completed'
2025-11-13 15:42:44.6686 IST [Polaris SCA Package Manager Scan] INFO: Provided value for resource 'polaris.test.sca.tests.scaPackage.artifacts.path'
2025-11-13 15:42:44.6689 IST [Polaris SCA Package Manager Scan] INFO: Adapter finished
2025-11-13 15:42:46.1493 IST [Polaris Artifacts Uploader] INFO: uploading artifact for "SAST(sastFull)" assessment with id "af575147-7cc9-42c8-9734-87f892c8cb7b"
2025-11-13 15:42:46.1503 IST [Polaris Artifacts Uploader] INFO: uploading artifact for "SCA(scaPackage)" assessment with id "d0db7e66-8211-45b0-b26e-4d834d291dd7"
2025-11-13 15:42:47.4577 IST [Polaris Artifacts Uploader] INFO: Uploading artifact /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/idir.zip for "SAST(sastFull)" assessment
2025-11-13 15:42:47.5151 IST [Polaris Artifacts Uploader] INFO: Uploading artifact /Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/blackduck-sca-artifacts.zip for "SCA(scaPackage)" assessment
2025-11-13 15:42:48.1676 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact:   6%  16384/240698
2025-11-13 15:42:48.1720 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastFull)" artifact:   1%  16384/1548948
2025-11-13 15:42:48.3809 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact:  34%  81920/240698
2025-11-13 15:42:48.3812 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact:  61%  147456/240698
2025-11-13 15:42:48.8030 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact:  88%  212992/240698
2025-11-13 15:42:48.8032 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SCA(scaPackage)" artifact: 100%  240698/240698
2025-11-13 15:42:49.0150 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastFull)" artifact:  26%  409600/1548948
2025-11-13 15:42:49.2287 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastFull)" artifact:  51%  802816/1548948
2025-11-13 15:42:49.2373 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastFull)" artifact:  76%  1179648/1548948
2025-11-13 15:42:49.4695 IST [Polaris Artifacts Uploader] INFO: Uploading Progress of "SAST(sastFull)" artifact: 100%  1548948/1548948
2025-11-13 15:42:49.5027 IST [Polaris Artifacts Uploader] INFO: successfully uploaded artifact "/Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_sca_package_manager_scan/blackduck-sca-artifacts.zip"
2025-11-13 15:42:49.9889 IST [Polaris Artifacts Uploader] INFO: successfully uploaded artifact "/Users/madhusud/Jenkins_Testing/Nodes/workspace/Polaris_Arbitrary_Sast_Scan_main/nodejs-npm/.bridge/polaris_coverity_capture/idir.zip"
2025-11-13 15:42:50.0012 IST [Polaris Artifacts Uploader] INFO: successfully resumed "SCA(scaPackage)" assessment with id "d0db7e66-8211-45b0-b26e-4d834d291dd7"
2025-11-13 15:42:50.4488 IST [Polaris Artifacts Uploader] INFO: successfully resumed "SAST(sastFull)" assessment with id "af575147-7cc9-42c8-9734-87f892c8cb7b"
2025-11-13 15:42:50.4824 IST [Polaris Artifacts Uploader] INFO: Provided value for resource 'polaris.test.sca.tests.scaPackage.artifacts.uploadSuccessful'
2025-11-13 15:42:50.4834 IST [Polaris Artifacts Uploader] INFO: Provided value for resource 'polaris.test.sast.tests.sastFull.artifacts.uploadSuccessful'
2025-11-13 15:42:50.4847 IST [Polaris Artifacts Uploader] INFO: Adapter finished
2025-11-13 15:42:50.8020 IST [Polaris Waiter] INFO: Waiting for test with assessment type "SAST(sastFull)" and id "af575147-7cc9-42c8-9734-87f892c8cb7b"
2025-11-13 15:42:50.8026 IST [Polaris Waiter] INFO: Waiting for test with assessment type "SCA(scaPackage)" and id "d0db7e66-8211-45b0-b26e-4d834d291dd7"
2025-11-13 15:42:51.5687 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SAST(sastFull)" and id "af575147-7cc9-42c8-9734-87f892c8cb7b" is "Queuing"
2025-11-13 15:42:51.5697 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SCA(scaPackage)" and id "d0db7e66-8211-45b0-b26e-4d834d291dd7" is "Queuing"
2025-11-13 15:43:01.9160 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SAST(sastFull)" and id "af575147-7cc9-42c8-9734-87f892c8cb7b" is "Scanning"
2025-11-13 15:43:01.9420 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SCA(scaPackage)" and id "d0db7e66-8211-45b0-b26e-4d834d291dd7" is "Scanning & Publishing"
2025-11-13 15:43:22.5725 IST [Polaris Waiter] INFO: test with assessment type "SCA(scaPackage)" and id "d0db7e66-8211-45b0-b26e-4d834d291dd7" completed successfully
2025-11-13 15:45:05.6897 IST [Polaris Waiter] INFO: Polling Test Manager: state of test with assessment type "SAST(sastFull)" and id "af575147-7cc9-42c8-9734-87f892c8cb7b" is "In Progress"
2025-11-13 15:45:16.0142 IST [Polaris Waiter] INFO: test with assessment type "SAST(sastFull)" and id "af575147-7cc9-42c8-9734-87f892c8cb7b" completed successfully
2025-11-13 15:45:16.0411 IST [Polaris Waiter] INFO: Provided value for resource 'polaris.test.sast.tests.sastFull.completed'
2025-11-13 15:45:16.0414 IST [Polaris Waiter] INFO: Provided value for resource 'polaris.test.sca.tests.scaPackage.completed'
2025-11-13 15:45:16.0420 IST [Polaris Waiter] INFO: Adapter finished
2025-11-13 15:45:17.8061 IST [Polaris Policy Checker] INFO: Checking for policy violations for "SAST(sastFull)" assessment...
2025-11-13 15:45:17.8065 IST [Polaris Policy Checker] INFO: Checking for policy violations for "SCA(scaPackage)" assessment...
2025-11-13 15:45:18.8352 IST [Polaris Policy Checker] INFO: no policies were violated to break the build
2025-11-13 15:45:18.8757 IST [Polaris Policy Checker] INFO: Adapter finished
2025-11-13 15:45:19.1990 IST [Polaris Issues Fetcher] INFO: Fetching issues for "SAST(sastFull)" assessment
2025-11-13 15:45:19.1996 IST [Polaris Issues Fetcher] INFO: Fetching issues for "SCA(scaPackage)" assessment
2025-11-13 15:45:19.9522 IST [Polaris Issues Fetcher] INFO: Successfully fetched issues for assessment type "SCA(scaPackage)" with id "d0db7e66-8211-45b0-b26e-4d834d291dd7"
 {
 "critical": 6,
 "high": 109,
 "informational": 0,
 "low": 15,
 "medium": 133
}
2025-11-13 15:45:19.9619 IST [Polaris Issues Fetcher] INFO: Successfully fetched issues for assessment type "SAST(sastFull)" with id "af575147-7cc9-42c8-9734-87f892c8cb7b"
 {
 "critical": 0,
 "high": 2,
 "informational": 0,
 "low": 25,
 "medium": 13
}
2025-11-13 15:45:19.9900 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.informational'
2025-11-13 15:45:19.9905 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.critical'
2025-11-13 15:45:19.9909 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.high'
2025-11-13 15:45:19.9921 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.low'
2025-11-13 15:45:19.9926 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.issues.medium'
2025-11-13 15:45:19.9930 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.issues.low'
2025-11-13 15:45:19.9935 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.issues.medium'
2025-11-13 15:45:19.9939 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.issues.critical'
2025-11-13 15:45:19.9944 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.issues.high'
2025-11-13 15:45:19.9948 IST [Polaris Issues Fetcher] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.issues.informational'
2025-11-13 15:45:19.9955 IST [Polaris Issues Fetcher] INFO: Adapter finished
2025-11-13 15:45:20.3010 IST [Polaris Status Provider] INFO: Results for test "SAST(sastFull)" with ID "af575147-7cc9-42c8-9734-87f892c8cb7b" are available at https://poc.polaris.blackduck.com/portfolio/portfolios/edf596d3-b54f-4a6b-9e5c-209f2e526c67/portfolio-items/7387b9d0-a429-4ec6-9786-05de8fcb387c/projects/bdd2e557-f854-4ea3-8215-8c18a49d9879/tests/af575147-7cc9-42c8-9734-87f892c8cb7b/detected-issues
2025-11-13 15:45:20.3016 IST [Polaris Status Provider] INFO: Results for test "SCA(scaPackage)" with ID "d0db7e66-8211-45b0-b26e-4d834d291dd7" are available at https://poc.polaris.blackduck.com/portfolio/portfolios/edf596d3-b54f-4a6b-9e5c-209f2e526c67/portfolio-items/7387b9d0-a429-4ec6-9786-05de8fcb387c/projects/bdd2e557-f854-4ea3-8215-8c18a49d9879/tests/d0db7e66-8211-45b0-b26e-4d834d291dd7/detected-issues
2025-11-13 15:45:20.3016 IST [Polaris Status Provider] INFO: Polaris issues view for project "arbitrary-params-sast", branch "main" is available at https://poc.polaris.blackduck.com/portfolio/portfolios/edf596d3-b54f-4a6b-9e5c-209f2e526c67/portfolio-items/7387b9d0-a429-4ec6-9786-05de8fcb387c/projects/bdd2e557-f854-4ea3-8215-8c18a49d9879/issues?branchId=26a334dd-2d72-48c6-92e2-9734ac05b3d5
2025-11-13 15:45:20.3119 IST [Polaris Status Provider] INFO: Provided value for resource 'polaris.test.SAST.tests.sastFull.summary.url'
2025-11-13 15:45:20.3120 IST [Polaris Status Provider] INFO: Provided value for resource 'polaris.test.SCA.tests.scaPackage.summary.url'
2025-11-13 15:45:20.3122 IST [Polaris Status Provider] INFO: Provided value for resource 'polaris.project.issues.url'
2025-11-13 15:45:20.3124 IST [Polaris Status Provider] INFO: Adapter finished
******************************* END EXECUTION OF BRIDGE CLI *******************************
[Security Scan] INFO: Retrieving the issue count from the scan results
[Security Scan] INFO: Total issues found: 303
[Security Scan] INFO: Security Scan execution is successful
**************************** END EXECUTION OF BLACK DUCK SECURITY SCAN ****************************
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // script
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Declarative: Post Actions)
[Pipeline] echo
Black Duck Logs Publisher - Starting log upload process
[Pipeline] echo
Configuration: [githubOrg:polaris-jenkins-samples, repoName:arbitrary-params-sast, credentialsId:github-pat-logs-publisher, maxRetries:3, retentionCount:5, jobNamePrefixes:[MBP_Github_, MBP_, Github_, Pipeline_, Job_, Build_]]
[Pipeline] echo
Job Name: MBP_Github_Polaris_Arbitrary_Sast_Scan/main
[Pipeline] echo
Build Number: 3
[Pipeline] echo
GitHub Organization: polaris-jenkins-samples
[Pipeline] withCredentials
Masking supported pattern matches of $GITHUB_TOKEN
[Pipeline] {
[Pipeline] echo
Using configured repository name: arbitrary-params-sast
[Pipeline] echo
Target repository: polaris-jenkins-samples/arbitrary-params-sast
[Pipeline] echo
LogProcessor: captureJenkinsLogs called
```

---

*Log generated by Black Duck Logs Publisher*