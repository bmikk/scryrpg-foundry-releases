# ScryRPG closed-beta guide

> **This is an alpha build.** It is an early test version for the ScryRPG closed beta, not a
> finished release. It can damage a Foundry world, so back up your world before installing it,
> and before each session while you use it. It only connects for ScryRPG parties invited to the
> closed beta.

## What this is

ScryRPG adds a campaign panel and character sheet inside Foundry. Linked characters stay
in step with the ScryRPG website both ways: inventory, containers, the party stash, coins,
shops, loot, the library, and history with undo are together where you play.

## What you need

1. Use Foundry 13 with D&D 5e 5.3 (5.3.0 through 5.3.x), or Foundry 14 with D&D 5e 6.0
   (6.0.0 through 6.0.x). Foundry 14 also accepts the 5.3 line. Other D&D 5e versions
   are not supported by this beta.
2. Open Foundry at an `https://` address, or on `localhost`. Sign-in needs this;
   an ordinary `http://` address on your home network will not work.
3. The ScryRPG server address must use `https://`.
4. Everyone needs their own ScryRPG account and membership in the same party on the
   website. The Foundry GM must also be that party's GM on the website.

Two-browser testing used Foundry 13.351 with D&D 5e 5.3.3, and Foundry 14.368 with
D&D 5e 6.0.5, in Chromium 152. Foundry 14.368 with D&D 5e 5.3.3 passed separate panel and
sheet checks. Other versions and browsers are not yet verified. The menu instructions below
use Foundry 13.

## Back up first

1. Before installing, make a world backup. Even better, try the beta on a copy of your
   world first. Restoring a backup is the real undo if something goes wrong.
2. In Foundry 13, leave the world with **Game Settings → Return to Setup**. On the
   Setup screen, right-click your world and choose **Take Backup**. Wait for it to finish.
3. Alternatively, stop Foundry completely and copy your world's folder from
   `Data/worlds` to somewhere safe. Keep the whole folder, not just selected files.
4. If a service hosts your world, use its backup or export feature. Keep the backup
   somewhere you can find again, and check how that host restores it.
5. To restore a Foundry backup, return to Setup, open the world's menu and choose
   **Manage Backups**. Find the backup from before installation, choose **Restore**,
   and confirm. This replaces the world's current state: later play in that world is lost.
6. To restore a folder copy, stop Foundry, move the current world folder aside, and put
   the saved folder back in its place under `Data/worlds`. Start Foundry again. For a hosted
   backup or export, follow your host's restore instructions.

A world backup restores Foundry, not changes already made on the ScryRPG website.
Leave the module disabled after restoring while we help you check what happened.

## Install

1. On Foundry's Setup screen, open **Add-on Modules** and click **Install Module**.
2. Paste this link into **Manifest URL** and click **Install**:
   `https://github.com/bmikk/scryrpg-foundry-releases/releases/latest/download/module.json`
3. Later versions arrive the same way: on **Add-on Modules**, click **Update** (or
   **Update All**) when Foundry offers one. Back up your world before updating.
   If Foundry says **Update the ScryRPG module to … or later**, ScryRPG needs that version.
   Until the module is updated, the panel still shows ScryRPG, but this world and ScryRPG don't
   sync: changes made in Foundry are kept and go up after the update.
4. Without the link, unpack the zip from the same releases page into a folder named
   `scryrpg-foundry` inside Foundry's `Data/modules` folder, so that the result is
   `Data/modules/scryrpg-foundry/module.json`. A hosting service's file manager works too.
   Restart Foundry, or return to Setup, so it sees the module.

## Turn it on

1. Launch your world as GM. Open **Game Settings → Manage Modules**.
2. Enable **ScryRPG Connected Campaign (Alpha)**, click **Save Module Settings**, and reload
   when prompted.
3. The server address already points at ScryRPG in a new world. Leave it alone unless
   we tell you otherwise. A world that used this module before keeps its saved address.

## Connect, once per person

1. In **Game Settings**, click **Open ScryRPG Campaign**.
2. In the panel, open **Account → Connect your ScryRPG account**. Click
   **Open the ScryRPG website**. While signed in to your own account, enter the code
   shown in Foundry (**Copy** copies it) and approve the connection on the website. The GM
   connects first and approves the world's connection to the party there.
3. Every player repeats this on their own computer with their own account. A GM cannot
   connect for a player. Keep the GM connected while the table uses ScryRPG.
4. Players open **Your character**. GMs and managers open **Your table** to see who is ready
   and who needs help. **Status** now shows sync health.

### Your table (GM)

Each player has one row with their character, what is happening, and at most one next action.
The count beside **Your table** tells you how many rows need you. Watching players do not count
as characters ready to play. If the connection has not supplied a fact yet, the table says it is
still checking.

- **Give <player> the sheet** answers their saved request. If they could not see a sheet to
  name, choose one from the short list first. They must connect with their own Foundry user
  before ownership can be verified. Existing permissions are preserved.
- **Set up for <player>** opens the same three questions with a banner naming the player.
  You can choose a sheet in this world, including a placeholder you own. Linking their existing
  ScryRPG character keeps it theirs. Creating one from a Foundry sheet first makes it yours,
  then sends them an offer. The row waits for their acceptance; it does not transfer it silently.
- **Copy invite link** appears when ScryRPG supplies a party join link.
- A problem expands in its player's row. **Keep this one** keeps the selected linked sheet;
  the other keeps its contents and permissions in Foundry and stops syncing. If the selected
  copy needs a new link, the same action connects it. An interrupted repair stays on the row
  for you to retry; opening the panel alone never restarts it.

World problems appear above the rows. If another browser is saving a character, close that
browser's character session, then reload here. There is no takeover button.

Pending character offers appear on the recipient's **Your character** card. Choose **Accept**
or **Decline**. After acceptance, the normal sync grants access to the new owner's verified
Foundry user. A stale offer explains why it disappeared; a character limit shows the counts.

Use **Play a character yourself** for your own character. **Advanced** opens character switching, ownership, earlier versions, sync details and table
options. Problems appear inside the affected row, with one decision and one action.

### Your character

Players open **Your character → Connect my character**. The wizard asks at most three questions:

1. **Which character are you playing?** Choose your ScryRPG character in this party, or choose
   **It's not on ScryRPG yet** to start from a Foundry sheet. One character syncs at a time.
2. **Is it already in Foundry?** Choose a sheet you own, or **No, make it for me**. Your GM's
   Foundry builds a new sheet from ScryRPG. **Don't see your sheet?** lets you ask your GM for it.
   The request says **Saved** only after it is stored; it stays on your card and can be cancelled.
   A private sheet's contents are never shown to someone who cannot see it.
3. **Which version matches now?** When both copies have meaningful data, compare their level,
   hit points, items, coins and last-changed dates. Neither version is chosen for you. Pick one
   whole version; the preview names fields that cannot switch.

Before replacing an existing Foundry sheet, setup waits for the GM to save and verify its backup.
Keep the wizard open while waiting, or reopen it to check the saved attempt after a reload.
If either version changes before setup starts, review again. Uncertain operations keep their
original identity rather than starting another copy.

Items are paired automatically only when their native identities prove a match. Ambiguous items,
including two same-named items, remain unlinked on your sheet and are listed as **Kept only in
Foundry**. Explicit item-pairing tools are reserved for Advanced.

**Ready** means the sheet has arrived, you own it, and its level-up work is complete. Otherwise,
the card names the remaining step: **Finish level-up**, **Waiting for your GM**, or **Items still
arriving**. Once ready, use **Open sheet** and play normally. **Something wrong? Get help** copies
a diagnostic report. **Advanced** opens switching, earlier versions, comparison, unlinking and a support report.

If ScryRPG asks which character you play now, the current default is preselected.
**Keep <character>** confirms the choice; **Ask me later** leaves the default in place. Other sheets stay in
Foundry and stop syncing until you switch back. If your GM handles setup for the table, your card
says so and offers **Ask** instead of the self-service wizard.

If a sheet is linked but its version choice is unfinished, **Finish connecting**
opens directly at the version question. You do not have to select the same character and sheet again.

On a shared computer, sign out from the Account menu when you finish.

## Using it

1. **Home** shows the party at a glance, with each character's ScryRPG picture (or their initials
   when they have none). Choosing a character in the left rail makes it the one
   you act as: for purchases, for where items go, and for Activity's filter. From Home, the
   Library or the GM tools, it also opens that character's inventory. **Open sheet** opens
   its sheet.
2. **Inventory** keeps the **My character**, **Party** and **Stash** scopes. Party shows
   character cards on the left and a separately scrolling Party Stash on the right. In a narrow
   panel, use **Characters | Party Stash** tabs. Items without a container appear under **Unsorted**
   in the stash.
   - **Find an item** searches names and tags from two characters. **Expand all** and
     **Collapse all** adjust the cards and containers without jumping the scroll position.
   - Players initially see their own characters and nonempty containers open; GMs start with
     characters collapsed. Small stash containers start open. Expansion lasts while the panel is open.
   - A container’s **…** menu switches between list and cards view, or opens container editing
     on ScryRPG. Narrow panels always use lists.
   - Rows show weight for one item and value for the whole stack; hover the value for its unit
     value. Click a row for details, including the existing split, equipment and commerce actions.
   - Each item's **…** menu offers **Edit Details**, **Split Stack** for multiple items, and
     **Remove Item**. Removing asks first and sends the item to party trash; undo it from History.
     Edit changes name, quantity, unit value and weight, with served equipment/attunement toggles
     for character items. **Add custom item** beside catalogue Add creates an item in that container.
     Owners can manage their characters, GMs/managers can manage all characters, and members can
     manage the Party Stash. GMs can download **Export CSV** for the party inventory.
   - **Move** opens **To**, then **Container**; quantity starts at one. **Give** remains in **…**.
   - Drag an item to a container, character header or Party Stash header. Other cards collapse
     while you carry it. Hold a collapsed character or an inactive tab for just over a second to
     open it. Releasing or pressing Escape restores the layout. Stacks ask how many to transfer,
     starting with the whole stack. ScryRPG decides cross-container merges; merging stacks within
     the same container sends Merge when the stacks are compatible.
   - **… → Use ScryRPG portrait in Foundry** sets the character's Foundry picture from ScryRPG,
     when ScryRPG has one. **Open on ScryRPG** reaches container management on the website.
   - **Funds** is your money. **Adjust currency (+/−)** adds or removes coins; a negative amount
     removes them. Coins also show as items in the container that holds them.
3. **Shops** lists the party's shops. In a shop, set **Buying into** once: a character's container
   or the Party Stash. It is also where **Sell** takes items from. **Buy** or **Sell** opens a
   dialog with ScryRPG's price. Choose **Pay with** (the character's funds or the party's) and a
   quantity, then confirm. If the price changes before you confirm, the dialog asks again.
4. **Loot** lists the party's loot piles. **Take** opens a dialog: how many, and where to put it,
   including the Party Stash. The GM can **Reveal** or **Hide** a pile. Piles that use need/greed
   are voted on the website.
5. **Library** searches the items your table can add. **Table library** shows what your table can
   use; **All content** also shows items outside your table's shelf. Open an item to see it, then
   **Add to…** to choose a container and a quantity. **Add item** on a container opens the
   Library for that container.
6. **Activity** is the party's timeline. Search it, filter it by **Items**, **Shops**, **Loot** or
   **Other**, or choose a character in the rail. Click an entry to see it in **History**.
7. **History**, on each character sheet and on Home, lists changes with **Undo** where it is
   offered. This undoes individual changes; it does not replace your world backup.
8. The character sheet has **Stats**, **Spells**, **Inventory**, **Notes**, **About** and
   **History**. Use it for rolls, hit points, spells, rests and equipment. **Currency** sets the
   exact number of coins.
9. The **Open on ScryRPG** icon, at the top right of a character, a container, a shop, a loot pile
   or the Library, opens it on the website: use it for anything the panel doesn't do. A container
   or item opens its owner's inventory there.

## Re-importing from D&D Beyond

1. Re-import a linked character when you want to update its build: classes and levels,
   abilities, proficiencies, features, spells and maximum HP come from D&D Beyond.
2. Play keeps the table's values: current and temporary hit points, coins, items, death saves,
   exhaustion, inspiration, spent spell slots, spent hit dice and spent feature uses.
   The importing player receives one private message saying what was kept.
3. Conditions reset to D&D Beyond's conditions, usually none. Reapply active conditions
   after the re-import. Between sessions is a good time to do this.

## The recommended way to play in this beta

1. Give each kind of change one home:
   - During a session, make changes in Foundry: hit points, spell slots, using items, and
     moving gear and coins in the panel or on the sheet.
   - Create shops and loot on the website, before or during the session, and use them in
     Foundry.
   - Level up between sessions, with the sheet's level-up button or a D&D Beyond re-import,
     not both for the same level. A level-up on the website shows in Foundry as waiting.
   - Avoid editing a character on the website while the session is running. The module copes,
     with notices and undo, but it's the likeliest source of surprises.
2. The GM opens the world first and leaves last. Changes made on the website reach Foundry only
   while a GM who has connected their ScryRPG account has the world open. Nothing is lost while
   no GM is in; it arrives when the GM next opens the world.
3. Everyone connects before game night. Each player signs in once with their own account and
   links their character then, not at the start of a session.
4. Back up the world before each session while the beta lasts.
5. Start small: run the first session on a copy of the world, or with one or two linked
   characters, before linking the whole party.
6. If you use D&D Beyond Importer's options that send changes back to D&D Beyond, turn them off
   for linked characters during the beta, so changes flow one way: from D&D Beyond into Foundry,
   and between Foundry and ScryRPG.
7. If something looks wrong, pause sync rather than fixing it by hand in both Foundry and the
   website, which creates competing changes. Then tell us (see below).

## Known limits in this beta

1. Conditions do not sync with ScryRPG in either direction. Set them in Foundry for play.
2. Experience points, and uses or charges spent on items and features, stay in Foundry.
   ScryRPG doesn't keep them yet, so awarding XP in Foundry (by hand or with a module such as
   Monk's TokenBar) is fine, and the website won't show it.
3. Carrying capacity reads **Capacity not shown** in the panel, or **Not shown** where
   the value is unavailable. The Take dialog omits unavailable capacity. Loot piles show no total value.
4. Create shops and loot on the website, then use them in Foundry. For voting on loot,
   the panel says **This pile uses need/greed: vote on ScryRPG**. The hero’s **Open on ScryRPG**
   icon opens that pile for voting and management.
5. Loot placed on the map, journals and lore, and encounters are not in this version.

## If something goes wrong

Report problems to the ScryRPG team in the closed-beta channel where you were invited.
Open the campaign panel’s **Account** menu to find the installed ScryRPG module, Foundry and game
system versions. Press **Copy diagnostics** and include that text with your report. It includes
connection and world status, any world hold reason, setup progress and counts of stale links and
pending changes. It excludes account details, names, IDs, URLs and sign-in secrets. If copying
fails, select and copy the diagnostics text shown in Account. A GM’s and an affected player’s
blocks can help explain a table-wide problem.

1. As GM, open **Game Settings → Configure Settings** and turn on **Pause ScryRPG sync**,
   then save. This stops sending and applying ScryRPG changes; it does not undo earlier ones.
   The panel also offers **Account → Pause sync**. When ready, the GM can use
   **Advanced → Sync → Resume sync**.
2. To stop using the module, open **Game Settings → Manage Modules**, uncheck
   **ScryRPG Connected Campaign (Alpha)**, click **Save Module Settings**, and reload.
3. To put the world back as it was, restore the backup using the steps above.
4. Tell us what you did and roughly when. Press **F12**, open the browser console, and
   send a screenshot of any errors. Never share sign-in codes; hide them in screenshots too.

## Uninstalling

1. Disable the module as above, or remove it from Foundry after leaving the world.
2. Its notes on characters and items, items it created, and a few settings stay in the
   world. These leftovers are harmless. Removing the module does not put earlier values back.
3. The backup is the only complete undo for the Foundry world.


## Advanced

Open **Advanced** from Your character or Your table for switching characters, reviewing every
difference, fixing item matches, restoring an earlier version, unlinking, and copying a support
report. Unlink keeps both the Foundry sheet and ScryRPG character. The GM also has table-wide
sync, held-deletion, history, ownership and world options here.

**Foundry backups.** The module saves a verified copy of a Foundry sheet before anything replaces
it, and **Save a backup now** saves one whenever you like. The last 3 are kept. Players' backups are
written by the GM's browser, so they show **Waiting for the GM** until a GM is in the world.

**Restoring a Foundry backup** changes only the Foundry sheet; it never sends anything to ScryRPG.
It works on a sheet that isn't syncing. To restore a character that is syncing, choose **Stop
syncing <name> · Unlink…** first, restore, then connect it again with **Connect my character** and
choose which version to keep. Restore always shows a preview first and saves the current sheet
before replacing it.

**ScryRPG restore points** protect the ScryRPG character when you choose to keep the Foundry version
during setup. When ScryRPG can save them, that restore point also keeps hit points, conditions and
spell slots; when you restore it, the preview offers **Also bring back hit points, conditions and
spell slots**, ticked by default. A changed character needs a fresh preview and confirmation. Hidden values stay hidden.

**Stop syncing** turns a sheet into a plain Foundry sheet: it keeps everything on it and ScryRPG
keeps its character. **Two sheets for one character:** when a character has two Foundry sheets,
your table shows it; choose **Keep this one** and the other becomes a plain Foundry sheet.

Wild Shape and Polymorph forms never sync; the original character is unchanged.

**Give to…** offers a character to another party member. After acceptance, the GM reviews whether
the former owner should keep Foundry Owner access. **Table options** controls whether players may
connect their own character and whether the party's sheets have default Observer access.
