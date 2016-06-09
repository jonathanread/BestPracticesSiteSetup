# BestPracticesSiteSetup
This module sets up sitefinity in my "huge" opinion best practice. Note that this is using Sitefinity 9, but can be used with any version greater than 8, just modify the nuget package reference to use the version you have.
##Using this module
Download the project
add it to your solution
change nuget reference to match your version of Sitefinity
add reference to this in SitefinityWebApp
build
Install module from Admin portal Administration > Modules & Services > BestPracticeSiteSetup
This will modify the configs as pointed out below

##This Module Does
###Pages
-Turns of inline page editing
-Sets groups pages to redirect to first accesible child page
-Sets "home" page to redirect to site root "/" 
###Caching
-Sets OutputCache Profiles to WaitForPageOutputCacheToFill=true
-Sets "Long Cache" profile duration to 24 hours 
###Security
-Sets password reset = true
-Sets password retrievel = true

For the security items like reset to work you need to make sure you have your SMTP setup and set the recoveryMaillAddress in Settings > Security > MembershipProviders > Default > Parameters > recoveryMailAddress
