# Dereth Exploration Automation

This project contains a set of routes and meta profiles for
[VTank](http://www.virindi.net/wiki/index.php/Virindi_Tank)
with the goal to automate the [Dereth Exploration](http://acpedia.org/wiki/Dereth_Exploration) quest series.

## I want to use these, what do I do?
All .met files are self-contained. Just download the one(s) you want, put them into your VTank installation folder,
log in to the game and they should be available and functional.

To be clear: If you just want to use these, only download the .met file you want.
You do *not need to download individual routes* to use a .met file.

It is recommended that you use a profile that contains all life buffs and at the very least BPS banes.
You should not be burdened and certainly not defenseless!


## Known Issues
### All meta profiles
- You need Recall Aphus Lassel for any of the profiles to work
- The meta profile will set the following default values in your profile:
  - ApproachDistance 0
  - AttackDistance 4
  - UsePortalDistance 0.018
  - NavFarStopRange 20

### Party-Goer
- The marker at Banderling Castle requires combat to be reached reliably due to too many mobs in the path. It is recommended to have only slash weapon in your profile

## I want to help, what do I do?

Fork this project, add/update routes or meta profiles and make a pull request. Please make sure your commits as well as the pull request have useful comments explaining all changes or additions.

### Contributing to routes
- All routes need to start with a 10 second pause followed by Recall to Aphus Lassel or another quest recall
- Always use AL recall if there is a route from Town Network, even if using a different recall would be shorter or faster. The goal is to keep the requirements as minimal as possible!
- It is recommended to put a 5 second pause after the use of portal. This seems to prevent some issues on bad connections.
- Route names should start with xploreTo 
- It is better to run around a narrow passage than to "lag thru" it

### Contributing to meta profiles
- Always start by flagging and end at Sean the Speedy in Holtburg. Use the ExplorationTemplate profile as a template.
- When adding or modifying embedded routes, make sure the route file is also added or updated. The only exception to this are routes with a single nav point to use a marker
- Name your states for navigating to a marker and using it similarly, e.g. goToMarker1 and useMarker1
- To use a marker, create a "circular" route to use it and follow it with state change based on a chat message matching "You have found a total of \d+ of the Exploration Markers."
