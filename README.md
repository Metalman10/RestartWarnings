# RestartWarnings
This is my first release and i thought i should help out and give back to the community. Heres a restart warning script i put together. Later on i am going to be supporting warning sounds that will play to ensure all players know that a restart is coming. No more excuses !

inside your InitServer.sqf (Located inside the root off the mission file)
[] execVM "EXPClient\EXP_RestartWarnings.sqf"

Now copy the contents of the download into your mission file! It should go Exile.Altis > EXPClient > EXP_RestartWarnings.sqf


CONFIGURE

//Set this to the amount of hours in your server restarts, pretty simple.
_ServerRestartTimeInMinutes = 240;			// 240 = 4 Hour restarts 180 = 3 Hour restarts

//Edit as you wish
		["toastRequest", 
		["ErrorTitleAndText", 
		["Restart Warning", format ["The server will restart in %1 minutes",_WarningOne]]] 
		call ExileServer_system_network_send_broadcast;
