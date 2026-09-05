# portainer-test

This USED to have an embedded test image. However it was moved to a seperate
repo, ghcr-test, to better simulate typical production use

So now this should only have the compose file.

This was mainly to clarify Portainer webhook behaviour.

Interestingly, it seems that Community Edition WILL auto-update from a mutable
tag, if the app source and the portainer stack source are in the same repo.
Presumably because it notices "oh, my stack source repo had a change!"

But if they are seperate and only the app repo changes, CE will NOT update 
from a webhook call. That requires Business Edition.
