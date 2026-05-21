# SpotZone
SpotZone would be a custom Nintendo Zone program that allows you to easily host a Nintendo Zone hotspot without needing a console to host it on. It would do this using an emulated version or custom reimplementation of the 3DS local wireless protocol (instead of using a custom Wi-Fi network), allowing unmodded 3DS consoles to connect.

## Features
### Easy Setup & Hosting
You would be able to easily create your own Nintendo Zone with a mix of official and custom content using a Nintendo Zone template (which I've already created, check out [this repo](https://github.com/AnonymousUser98/NintendoZoneTemplate)) and a built-in toolbox to help modify and customize the template.

### StreetPass Relay
During setup, the user would be asked if they want to enable StreetPass Relay (SPR). If they choose to enable it, then their SpotZone hotspot will have SPR functionality. It would have a few extra features, such as automatically filtering out cheated _Warrior's Way_ scores and banning users by adding their console to a blacklist. It could also have a "whitelist mode" that only allows whitelisted users to use SPR at your hotspot.

### SpotPass Distribution
I don't know if this would be possible to do, but it would be a great feature to have.

This feature would allow players to set up and distribute SpotPass content, including:
- Pokémon Mystery Gifts
- _Animal Crossing_ Items (custom homebrew items if possible)
- _Puzzle Swap_ Images
- Custom stationery for SwapNote
  - There would be a bunch of customizable built-in templates that allow you to easily add your own assets.
  - This might work by sending you a SwapNote message that uses the custom stationery. The message that it sends could be customized and turned into a collectable "postcard".
- Game demos (the user would need to provide the ROMs and check a box confirming that they're not using SpotZone commercially)

The SpotZone distribution app (that runs on a computer and hosts the SpotZone hotspot) would make it easy to do this with a bunch of built-in presets and item generators.

### DS Download Station
If the user provides the ROMs and imports them into the SpotZone desktop app, then it would make the SpotZone location double as a DS Download Station.

### Printable Posters
Included poster templates and generators would allow you to easily print posters that say stuff like "Nintendo Zone available here" or have instructions on how to connect.

### Archived Content
All the archived content from SatellaZone would be included, so you can easily have the official trailers and screenshots available.

## Web Interface
The project probably won't start with this, but I have some ideas about the Nintendo Zone pages and their functionality.

The home page (`index.html`) would be the same (with a custom logo/banner on the enter button), but the main menu page (`menu.html`) would be different. It would use the standard table layout (with 2 buttons on the top and 3 buttons on the bottom), but the content would be customized.

### The Top Row
The following buttons would be available for including in the top row (you can choose 2):

#### Game Demos
_An official asset exists for this button. It can be found in the template I created: [menu-promo/Promo_demos.jpg](https://github.com/AnonymousUser98/NintendoZoneTemplate/blob/main/menu-promo/Promo_demos.jpg)_

This would open a page explaining how to access the game demos through DS Download Play.

#### Preview Game
_Official assets exist for this button. Find them in the template repo._

This would open the Nintendo Zone details page for a chosen game.

This button could be used twice on the main menu.

#### Community Events
This button would open a page that shows upcoming events that are happening at or near the SpotZone location.

#### Free Gifts
This button would open a page about a SpotZone gift that can be received from within a game.
It could also open a page where you can get SwapNote stationery.

### The Bottom Row
The bottom row of the main menu would have these 3 buttons:

#### Games & Videos
_This button might use a custom asset, but it could also use the official "Explore Games" button._

This would open the `games/menu.html` menu, which would have the following options:
- **Preview Games** - Same functionality as the official Nintendo Zone websites.
- **Watch Videos** - Same functionality as the "Watch Videos" button on the official main menu page (opens a page with a list of videos).
- **Play Others Online** - Opens a page that tells you about the Pretendo Network (already created, find it in my template repo).
- One other option (to keep the original 2x2 grid layout), but I don't know what it would be.

#### Information Station
This would open a page that has a similar layout to the 3DS notifications menu. It would have a bunch of "task list"-style articles like "Learn about SpotZone", "Learn about Pretendo Network", "Get extra SwapNote stationery", and others. The desktop app would make it easy to create your own entries, which could be written articles, links to pages in the _Special Content_ section, or your own custom pages.

#### Special Content
This is where the SpotPass content (and in-game gifts) would be. It would show a list of games that have available content, and clicking on one would tell you how to receive the content (e.g. "open the game and choose the _Mystery Gift_ option on the title screen).
SwapNote stationery/postcards would be sent to your console when you initiate a download from somewhere in this section.

**THIS PAGE IS UNFINISHED.**
