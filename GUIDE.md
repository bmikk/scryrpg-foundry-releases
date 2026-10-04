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

Two-browser testing used Foundry 13.351, D&D 5e 5.3.3 and Chromium 152.
Foundry 14.368 with D&D 5e 6.0.5 and 5.3.3 passed separate panel and sheet checks,
but has not had the same two-browser testing. Other versions and browsers are not yet
verified. The menu instructions below use Foundry 13.

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
   shown in Foundry and approve the connection on the website. The GM connects first
   and approves the world's connection to the party there.
3. Every player repeats this on their own computer with their own account. A GM cannot
   connect for a player. Keep the GM connected while the table uses ScryRPG.
4. If Home shows **Finish character setup in Status**, click it. In **Status → Setup**,
   **Set up characters** shows what each character still needs and counts before you choose.
5. To link an existing Foundry character, select it under **Your Foundry character** for
   the matching ScryRPG character. Click **Compare with ScryRPG** and read the differences.
   Choose **Link it, keeping Foundry's values** or **Link it, keeping ScryRPG's values**
   according to which copy you want to keep.
6. If asked to match items, match each ScryRPG item to the same item in Foundry, or choose
   **Not in Foundry**. Review any **Remove from ScryRPG** choices and the items listed under
   **Sent to ScryRPG as new items**, then click **Start character setup**.
7. A Foundry character missing from the website can use **Create in ScryRPG**. Other setup
   prompts offer **Keep the Foundry side** or **Keep the campaign side** and explain what
   remains to do. Review any characters or items being replaced, then use **Carry out this choice**
   when offered.
8. If it says **Waiting for setup data**, keep the GM connected and follow the message.
   Resolve any **Conflict** shown before continuing. Setup is finished when it says
   **Foundry and ScryRPG agree; setup is complete.**

When the GM creates a character for a player, the GM gives that player ownership of it in Foundry.

On a shared computer, sign out from the Account menu when you finish.

## Using it

1. **Home** shows the party at a glance, with each character's ScryRPG picture (or their initials
   when they have none). Choosing a character in the left rail makes it the one
   you act as: for purchases, for where items go, and for Activity's filter. **Open sheet** opens
   its sheet.
2. **Inventory** has **My character**, **Party** and **Stash** views, with the Party Stash first.
   Expand a character or a container to see its items. Click a row for its details, and its
   picture for a larger view.
   - **Give** (the arrows icon) and **… → Move** open a dialog: choose where it goes, then how
     many (**1**, **Half**, **All** or a number).
   - Or drag a row onto a container. A stack asks how many. Dropping a row onto a character opens
     Move with that character chosen.
   - **… → Use ScryRPG portrait in Foundry** sets the character's Foundry picture from ScryRPG,
     when ScryRPG has one.
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

1. As GM, open **Game Settings → Configure Settings** and turn on **Pause ScryRPG sync**,
   then save. This stops sending and applying ScryRPG changes; it does not undo earlier ones.
   The panel also offers **Account → Pause sync**. When ready, the GM can use
   **Resume** in **Status**.
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
