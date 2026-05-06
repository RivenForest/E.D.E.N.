E.D.E.N. - Elite Dangerous Exploration Navigator (easier read in code view)

What is E.D.E.N.?
E.D.E.N. is an interactive Elite Dangerous companion designed for commanders to do something we haven't been able to do since the game started.  Simply put, share our data with friends, or the community, and KNOW where we've been.  What I mean by that is with E.D.E.N. a cmdr can finally ask "If I went in this direction, will I discover something new or run into a bunch of known space?"  That's it...that's the goal in a nutshell.  

I've also included a lite Colonization tool that will help cmdrs track active colonizations and fleet carrier(s) market(s)....because I could.  There's a lot of tools out there doing this...but instead of making someone use another tool I figured what the heck?  I'll add it so I did.  This is working at a rudimentary level now but I plan on fleshing it out further once I get the rest of the tool fully operational.
Why use this tool instead of everything else out there?
I'm not saying anyone should.  The goal of E.D.E.N. is not to replace other community tools.  We each have our own style and, quite frankly, quirks when it comes to gameplay.  I built E.D.E.N. simply because I was tired of trying to find out where I'd been, what I'd found, and how to get back to interesting places that I'd lost track of.  I was really tired of the bookmark pin-map my galaxy map had become.  A bookmark I made 6 months ago becomes a pin that I look at (from 10kly away) and go "Why the heck did I pin that?".

What I'm offering is a way for players who want to know more about where they've been, what they saw, and how to get back to it then E.D.E.N. will help you.  And, more importantly, if you're part of a group of friends, a wing, or an expedition you'll be able to share your data with anyone else that you want to and your instance of the tool will allow you to view/search/analyze that data as if you've been there yourself.  Eventually, for those that want to, you'll be able to use external data sources like SPANSH or EDSM  to import locally and see where, within a reasonable amount of time depending on your data import, other players in the game are currently concentrated vs where the galaxy is empty.  Letting you choose which direction to explore in with a bit more certainty that you'll be alone than you were before.

E.D.E.N. is designed around a local-first philosophy:

What does local first mean?  Simply put, if you have your old journals available on your system, the tool will read those journals into it's db and then allow you to actually use that data wihout any other tools needed.  Want to know how many ELW's you've found?  Easy.  Or maybe you want to find that one system that had ELW, water, and ammonia worlds...yup...this will find it for you.

The tool also uses logic to track "expeditions" in the game.  This is one I'm proud of.  Each time you jump the tool tracks you and, once you sell off your data (UC+VG) that expedition ends and a new one begins.  Then you jump around for a couple days, months, whatever...and crash.  You just lost all of the data and credits you've worked hard for, rage quit the game and go have a drink.  Been there, done that....but....E.D.E.N. see's you've crashed and immediately records that expedition as "Lost" and saves it.  You can then search that data and recover the valuable systems that were previously unrecoverable.  And unlike the game, where if you lost that data before you sold it, E.D.E.N. remembers ALL of it for you.  You might not get your Firsts (Discovered, Mapped, Footfall) but you'll still know you've been there.

E.D.E.N. is currently in active development.

I've built the GUI around what interests me in the game so far.  And it's got a lot more than just an archive of data going for it.  

Features so far:

Current Status Tab/Page - First to show

Quick Overview
The Current Status tab is designed to act like a live cockpit dashboard for your commander — showing who you are, where you are, what you’re flying, what you’re building toward, and whether the tool is actively keeping up with the game in real time.
More detailed exploration analysis, expedition reconstruction, body-by-body exploration data, and deeper colonization systems live in their own dedicated tabs..
Left Column
Commander Panel
This is the active cmdr playing the game (for those who have multiple accounts this auto-changes on game load).
Shows:
Commander name
Current (on ship /in SRV/on foot)
Credits on hand
Optional exobiology sales estimates (If Bioscan is installed)
Game version/edition
Current suit and loadout
Module slot information (WIP)
Useful for:
Quickly confirming your active commander
Checking your current location (ship/srv/on-foot)
Keeping track of unsold exobiology data (red text to show it's at risk until sold)

Location Panel
Your current position in the galaxy:
Region: (WIP) right now this is inferred from your journals and the last time you crossed a region boundary
Current star system
Discovery / first-discovered information (when available via EDSM lite pull)
Useful for:
Quickly identifying where you are

Active Colonization Panel
Summary view of your Tracked colonization systems
 -each system expandable for a concise picture of that system's status
Useful for:
Keeping colonization progress visible while flying
Remembering which carrier had the materials you needed
Avoiding the “wait…which site was I working on again?” problem
Middle Column
Ship Panel
This is basically your active ship overview and quick sanity-check panel. The goal here wasn't to recreate the in-game shipyard, it was to answer the question:
“Am I in the ship I think I'm in and is it configured the way I expect?”
Shows:
Ship name
Type
Registry/callsign
Ship status: Docked/in flight/grounded
Max Jump range
Cargo capacity
Current Value
Rebuy cost
Insurance warning indicators ( if you don't have enough credits on-hand for rebuy it highlights red)
Useful for:
Verifying your current ship setup
Checking jump capability before heading out
Making sure you can actually afford to explode
Carrier Panel
This is your Fleet Carrier summary area. If you own one, you'll know why this matters pretty quickly. If you don't own one but bounce around other peoples' carriers a lot, it's still useful for keeping track of where you parked yourself.
The goal here is to keep carrier context visible without needing to check in-game
Shows:
Carrier name
Registry
Current System
Last System
Planned Jump
Tritium/Fuel/Cargo summaries (WIP)
Budget balance (credits on ship)
Current Tax rates
Weekly upkeep (configured manaully from settings)
Weeks until FC maintenance fails (WIP - lets you know when you'll lose your FC unless you deposit more credits)
Useful for:
Keeping track of active carriers
Remembering carrier supply locations
Supporting colonization logistics
Avoiding carrier confusion after 14 jumps and no sleep
Right Column
NavRoute Panel
This is your plotted route through the galaxy. Right now it focuses on giving you a quick readable overview of your current travel path without needing to constantly jump back into the galaxy map.
Shows:
Next system in route
Remaining jumps

    Navroute table
Systems - system name
Distance - jump distance
Discovered - discovered by when available (lite EDSM pull)
Useful for:
Reviewing your current route
Tracking exploration progress
Planning upcoming jumps
Seeing where community exploration starts thinning out

System Messages Panel
This is less “chat log” and more “mission control status panel.” If something in the tool looks stale or weird, this is usually the first place to look before assuming something exploded.
Shows:
Journal/mirror activity
Plugin status (EDMC / ExploData / BioScan)
Catalog status summaries
Session activity indicators
Misc tool status information
Useful for:
Confirming the tool is actively receiving game data
Verifying plugin activity
Identifying stale sessions or disconnects
Knowing whether the problem is Elite or me breaking something again

Diagnostic Output (Dev tool/Hardcore players)
This is mostly for dev and test users. Normally this stays hidden unless diagnostics are enabled in preferences.
Shows:
Debugging information
Diagnostic output
Internal status traces
Useful for:
Troubleshooting
Debugging weird behavior
Watching the tool panic in real time

Bottom Quick Actions Area (Reserved)
There's a reserved strip at the bottom of the tab for future quick actions and contextual controls. Depending on the current build this may be empty or partially used.

