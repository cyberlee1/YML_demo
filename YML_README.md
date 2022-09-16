Help configure Pipeline

YML contains:
Stage: which contains multiple/collection of jobs
Jobs: which contains multiple/collection of Steps runs on agent/environment
Steps: which contains multiple tasks which help define the set of process or activity you want to perform/execute. 
Type of Steps could be Task, Script, Templatereference

Example of Hierachy YML file:

Stages:
	- Stage: Build
	Jobs:
	 -jobs: Build Package
	   Steps:
	   -Build
	   -Package
	   -Publish
	- Stage: Deploy/Test
	Jobs:
	 -job: StartDeployment
	   steps:
	   -DeployPackage
	
Schema(structured framework) of YML Pipeline file
Name: string #Define custom Build number/name
Variables: #Define variable for pipeline
Trigger: Trigger/none #To define which or number of branches to enable for CI
EXTRA: Pool: To define the agent or collection of Agent
Stages: [stage| template reference]
Jobs: [job| template reference]
Steps: [script| task| template reference]

Scenario
	- If the build is for single Stage and single jobs, no need to specifically put Stage and Job


NuGet package is a single ZIP file with the .nupkg extension that contains compiled code (DLLs), other files related to that code, and a descriptive manifest that includes information like the package's version number. Developers with code to share create packages and publish them to a public or private host. Package consumers obtain those packages from suitable hosts, add them to their projects, and then call a package's functionality in their project code. NuGet itself then handles all of the intermediate details.

From <https://docs.microsoft.com/en-us/nuget/what-is-nuget> 


After build is successful, go to terminal/cmdprompt
Git clone "your github website" in cmd prompt
It should save in your github in your computer
Once successfully in your VS, add /p:Configuration"
In cmd prompt
Code .
Git add .
Git commit -m "added release flag"
Git push
Github should prompt that you added the release flag
Adde status badge
