### Best Dota 2 Launch Options

**Enable Console**
 *-consoleOR+con_enable 1*
 -console will bring up the console as soon as you get into the game,  where as +con_enable 1 will simply enable it so it can be accessed via a hotkey, the default for which is ` (that’s the button to the left of  your 1 key). If you’ve rebound this button, you’ll need to go into the  options menu and make sure a not-easily-pressed key is bound to console. It’s in the bottom right hand corner of the hotkeys section. Personally I go with [.

That’s all you’ll need to use our console commands section later on, however there are other useful launch options too, like…

**Turn Off Intro Videos**
 *-novid*
 This disables the Valve intro video, saving you 3-4 precious seconds  every time you boot up the game. You also won’t get spooked when you  forget that his head turns around now.

**High CPU Priority**
 *-high*
 This gives the game high priority in the CPU, meaning it won’t be slowed down by other processes you might happen to have running. Useful on  slower machines where you want to keep a browser open at the same time.  Do be warned, messing with CPU priority can cause some odd things to  happen, so just be careful.

**Mouse Settings**
 *-useforcedmparms -noforcemaccel -noforcemspd*
 This trio of commands prevents the game from changing your mouse  sensitivity and acceleration settings, so it will use whatever Windows’  settings are.

**Reset Graphics Settings**
 *-autoconfig*
 If you have this enabled, every time you boot up the game it will reset  the graphics options to whatever the recommended ones for your hardware  are. This is useful if you manage to set it to some resolution your  monitor doesn’t recognise, or massively screw up in some other way.  Cheers, Valve.

**Faster Game Loading**
 *-map dota*
 This loads the map along with the game when you start, meaning you’ll  have a lower load time on your first match. Again, very useful for  frontloading that time so slower computers don’t take too long to get  into a game.

**Different Load Screens**
 *-dashboard[code]*
 A set of commands that will force the client to use the cosmetics of the various events that have run through the years. The possible codes are:

- international_2012 – Displays The International 2012 loading screen and main menu background.
- international_2013 – Displays The International 2013 loading screen and main menu background.
- international_2014 – Displays The International 2014 loading screen only.
- frostivus_2013 – Displays Frostivus 2013 main menu background.
- newbloom_2014 – Displays New Bloom 2014 loading screen and main menu background.
- spirits_2013 – Displays Three Spirits main menu background.

I’m personally quite partial to the TI2012 one. Do remember that  while this command is running you won’t ever see any sexy new loading  screens Valve introduces.

**Run In Windowed Mode**
 *-windowed*
 Boots the game in a window and *-noborder* makes it borderless. You can use…
 *-h[height]-w [width] -x [position horizontal] -y [position vertical]*
 To position where the window is on the screen. Again, this means you can customise these factors from outside the game and is useful for putting it on a second monitor, if necessary. For example, *-window -noborder -h 1920 -w 1080 -x 1921 -y 0* would have the game window fill a second 1080p monitor.

**OpenGL Mode**
 *-gl*
 Forces the game to run using the OpenGL graphics library.

**DirectX 9 Mode**
 *-dx9*
 Forces the game to run using DirectX 9, disabling several prettier graphics options. Useful on older computers.

### The Best Dota 2 Autoexec File Commands

**Bind keys to console commands**
 *bind “[key]” “command”*
 This lets you bind keys to various commands. It’s useful for quickly  getting your settings right on a new machine, as discussed above, but  also lets you bind console commands. That lets you do things like…

**Create keys to quickly look at runes**

This set of commands will bind F2 to look at the position of the map  where the top rune spawns while you hold the key down, moving back to  your hero when you let it go. F3 will be bottom rune.

*unbind F2*
 *unbind F3*
 *alias “+toprune” “dota_camera_set_lookatpos -2273 1800”*
 *alias “-toprune” “+dota_camera_center_on_hero;+dota_camera_center_on_hero;-dota_camera_center_on_hero”*
 *alias “+botrune” “dota_camera_set_lookatpos 3035 -2350”*
 *alias “-botrune” “+dota_camera_center_on_hero;+dota_camera_center_on_hero;-dota_camera_center_on_hero”*
 *bind F2 “+toprune”*
 *bind F3 “+botrune”*

Glancing at rune spots isn’t as useful as it once was (with there now always being one in each location) but you put*dota_camera_get_lookatpos*into the command line to find the camera coordinates of various useful  locations and decide which you’d like to be able to hit a button and  see. Here’s some we made earlier:

- Mid-lane: -487 -214
- Bot-lane: 6058 -4850
- Top-lane: -6105 5006
- Rosh pit: 4092 -1878
- Dire Secret Shop: 3608 355
- Radiant Secret Shop: -4384 1357

Just replace the numbers in the above example with these and you’re  good to go. Remember that you do also need buttons on your keyboard for  things like abilities, items and telling your team-mates just how bad  they are.

**Print current time in chat**
 *bind [key] “chatwheel_say 57”*
 This will print the current game time in chat for your team when the  corresponding button is pressed. Useful for keeping track of Roshan  spawns and the like.

**Bind team messages to keys**
 *bind [key] “say_team [phrase]”*
 This will bind whatever key you like to say whatever you want to your team. Don’t be mean.

**Bind keys for spectating
** *bind [key] “demo_goto -120 relative”
\* *bind[key]”demo_goto 120 relative”
\* These commands will move the seek bar in a demo backwards and  forwards by about 4 seconds. The number is ‘ticks’ and operates at about 30 a second. Test to see what you prefer for when you’re analysing  replays.

**Lower graphics settings**
 *dota_cheap_water 1*
 *cl_globallight_shadow_mode 0*
 *r_deferred_height_fog 0*
 *r_deferred_simple_light 1*
 *r_screenspace_aa 0*
 *mat_vsync 0*

This set of commands will turn off lots of graphics settings, making the game run better on older machines.

**Instant health removal**
 *dota_health_hurt_threshold 99999*
 *dota_health_hurt_decay_time_max 0*
 *dota_health_hurt_decay_time_min 0*
 *dota_health_hurt_delay 0*
 *dota_pain_decay 0*
 *dota_pain_factor 0*
 *dota_pain_fade_rate 0*
 *dota_pain_multiplier 0*

These will remove the scaling white bar that appears when a hero  loses health instead just immediately setting their health bar to the  new value. You can modify these numbers if you would prefer for the  white bar to be there but fade quicker. While we’re on health…

**Healthbar Settings**
 *dota_health_per_vertical_marker 250*
 decides how much health will be shown per vertical line on the health  bar. 250 is the default value. Axe players may wish for different ones,  for example. To turn the lines off entirely, set it to 99999.

**The Netgraph**
 *net_graphheight 64*
 *net_graphinsetbottom 437*
 *net_graphinsetleft 0*
 *net_graphinsetright -30*
 *net_graphpos 1*
 *net_graphproportionalfont 0*
 *net_graphtext 1*
 *bind F10 “showgraph”*
 *alias “showgraph” “showgraph_off”*
 *alias “showgraph_on” “net_graph 1; alias showgraph showgraph_off”*
 *alias “showgraph_off” “net_graph 0; alias showgraph showgraph_on”*

This set will place the netgraph, a useful set of ping readouts and  other network information, in the unused space at the top right of the  screen. F10 will toggle between it being on and off. It’s optimised for  1920*1080, so you might need to adjust some values if that isn’t your  resolution.

**Hide the Minimap**
 *dota_no_minimap 1*
 Hides the minimap.

**Dichromatic Minimap**
 *dota_minimap_simple_colors 1*
 Stops enemies and allies showing up in different colours on the minimap. All allied units are green, all enemy ones are red.

You can also customise how enemies, allies and neutrals appear on the minimap with these commands:

*dota_enemy_color_b ###*
 *dota_enemy_color_g ###*
 *dota_enemy_color_r ###*

*dota_friendly_color_b ###*
 *dota_friendly_color_g ###*
 *dota_friendly_color_r ###*

*dota_neutral_color_b ###*
 *dota_neutral_color_g ###*
 *dota_neutral_color_r ###*

These use standard blue/red/green colour definitions. Here’s a handy tool for finding out which colours are what.

**Flip the HUD**
 *dota_hud_flip 1*
 Moves the minimap to be in the bottom right hand corner of the screen.

**Colourblind Mode**
 *dota_hud_colorblind 1*
 Enables colour blind mode.

**Heroes More Visible On Minimap**
 *dota_minimap_hero_size 1000*
 Changes the size of hero icons on the minimap. The default is 600, 1000  or so makes it much more obvious out of the corner of your eye.

**Longer Pings On Minimap**
 *dota_minimap_ping_duration 3*
 Changes how long pings remain on the minimap for in seconds. 3 is the default value.

**Change the FPS Cap**
 *fps_max 120*
 Sets the maximum FPS for the game. 120 is the default value.

**Enable Range Finder**
 *dota_disable_range_finder 0*
 Turns on a little green line between your hero and cursor whenever you  start targeting an ability. If the line disappears you’re out of range.

**Enable Quick Self-casting**
 *dota_ability_quick_cast 1*
 Makes double tapping an ability or item button use it on yourself.

**Disable Auto-attack**
 *dota_player_units_auto_attack 0*
 Disables auto-attack for your hero.

**Right Click Denying**
 *dota_force_right_click_attack 1*
 Turns on ‘right click deny’ – you don’t have to press the attack key and then left click on friendly minions to hit them, you just right click  as you would on enemies.

**Prevent Minimap Misclicks**
 *dota_minimap_misclick_time 0.2*
 The time in seconds that the mouse must be over the minimap before a  move command can be issued. Prevents misclicks when running away. Set to 0 if you’d rather have an instantly responsive minimap, or 9999 if you  don’t want it to be usable at all.

**Disable Mousewheel Zoom**
 *dota_camera_disable_zoom 1*
 Makes it so you can’t zoom the camera in with the mousewheel.

**Disable Respawn Camera Move**
 *dota_reset_camera_on_spawn 0*
 Stops the camera from moving to your hero when you respawn.

**Disable Screen Shake**
 *dota_screen_shake 0*
 Disables the distracting screen shake when certain abilities are used.

**Enable Simple Ready Up**
 *dota_simple_ready_up 1*
 Removes the ready animation when a game pops and allows you to get in immediately.

**Enable The Console**
 *con_enable 1*
 If you aren’t using a launch option to enable the console, you’ll need this.

**Print Text To Console**
 *echo “[text]”*
 Prints text to the console. I’d recommend having a line at the end of your autoexec that’s something like of *echo “PREPARED FOR DIGITAL SPORTS”* – when you see that in the console you know your autoexec has ran  properly. If you end up with a particularly large autoexec it’s worth  splitting it into sections, each with their own echo command so you know which bits are loading properly.

### In-game Console Commands For Dota 2

**Reconnect To Games**
 *retry*
 This reconnects to the last server you were on.

**Show FPS Counter**
 *cl_showfps*
 Shows the FPS counter.

**Show Player Pings**
 *ping*
 Shows the ping of all players in the console.

**Show Net Graph**
 *net_graph 1*
 Shows the netgraph, if you’re not using the autoexec chunk from earlier.

### Dota 2 Cheat Commands

**Remember**: cheats only work on custom lobbies, do not even try to use them on an online match!

**Level Up**
 *-lvlup x*
 Increases your hero’s level by x. You can’t delevel this way, entering negative values won’t do anything.

**Level Bots**
 *-levelbots x*
 Increases bot heroes’ levels by x. See above.

**Give Gold**
 *-gold x*
 Gives your hero x unreliable gold. Negative numbers reduce it.

**Give Items**
 *-item [name]*
 Gives your hero the named item. You can see a list of item names on the [Dota 2 wiki](http://dota2.gamepedia.com/Cheats).

**Give Bot Items**
 *-givebots [name]*
 Gives bot heroes the named item. See above.

**Refresh Heroes**
 *-refresh*
 Restores the health, mana and cooldowns of all heroes on the map.

**Force Respawn**
 *-respawn*
 Respawns you. While alive, moves you to the fountain.

**Skip Warmup Phase**
 *-startgame*
 Immediately starts the game, causing creeps to spawn and such. Has no effect after the warmup period ends.

**Spawn Creep Wave**
 *-spawncreeps*
 Spawns a wave of creeps in each lane for both teams.

**Spawn Neutral Creeps**
 *-spawnneutrals*
 Spawns neutrals at their respective camps. Doesn’t ignore usual blocking rules.

**Stop Creep Spawns**
 *-disablecreepspawn*
 Stops the regular spawning of creeps in lanes. *-enablecreepspawn* renables it.

**Spawn Runes**
 *-spawnrune*
 Spawns runes at the runespots. One will be a bounty rune, the other a random non-bounty rune.

**Kill Wards**
 *-killwards*
 Destroys all placed Sentry and Observer wards on the map.

**Creat Heroes**
 *-createhero [name]*
 Creates the specified hero at wherever the mouse cursor is pointing. You can see a list of the codes for heroes on the [Dota 2 wiki](http://dota2.gamepedia.com/Cheats). If you add the “ neutral” or “ enemy” to the end it will create the hero for that faction, but still under your control.

**WTF Mode**
 *-wtf*
 All spells and items have no manacost or cooldown. -unwtf turns this mode off.

**Shared Vision**
 *-allvision*
 Radiant and Dire vision is shared. *-normalvision* disables this.