
#Research

##DisableBlipNameForVar()
Possible new name: `_GET_SELECTED_MISSION_CREATOR_BLIP`

Returns blip handle for mission creator blips only when they get selected on the pause menu map

Returns a value once when selecting the blip (or changing blips via the legend), must be listened for every frame

##N_0x4167efe0527d706e()
Possible name: `_HAS_SELECTED_MISSION_CREATOR_BLIP`

Returns true if hovering over a mission creator blip in the pause menu map

##N_0x3bab9a4e4f2ff5c7()
Possible name: `_IS_PAUSE_FRONTEND_VISIBLE`

Returns true whenever pause menu is open

Might have other criteria, but didn't seem to matter what page you had selected

##N_0xec9264727eec0f28()
Possible name: `_DISABLE_FRONTEND_INPUT`

Disables the front-end input (already documented kinda?)

Always used before changing frontend stuff

Not actually required, but seems to make sure player doesn't interact with half-implemented front-ends.

##N_0x14621bb1df14e2b2()
Possible name: `_ENABLE_FRONTEND_INPUT`

Re-enables the front-end input (already documented kinda?)

Always used after changing frontend stuff

Not actually required, but seems to make sure player doesn't interact with half-implemented front-ends.
