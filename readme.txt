=== Paid Memberships Pro: MemberPress Migration Toolkit Add On ===
Contributors: strangerstudios
Tags: pmpro, paid memberships pro, memberpress, migration
Requires at least: 5.0
Tested up to: 7.0
Stable tag: 0.1.1

Migrate your MemberPress members, subscriptions, levels, and content restrictions to Paid Memberships Pro with a guided step-by-step wizard.

== Description ==

Adds a toolkit page to help migrate MemberPress membership data to Paid Memberships Pro.

== Installation ==

1. Upload the `pmpro-memberpress-migration-toolkit` folder to the `/wp-content/plugins/` directory.
1. Activate the plugin through the 'Plugins' menu in WordPress.

== Changelog ==
= 0.1.1 - 2026-06-17 =
* ENHANCEMENT: User migrations are now queued in batches to avoid timeouts when migrating large sites. #9 (@dparker1005)
* ENHANCEMENT: Added dependency guards so the migration tools fail gracefully when Paid Memberships Pro is not active. #6 (@dparker1005)
* ENHANCEMENT: The Stripe Secret Key field on the Migrate Users step is now a password input. #13 (@dparker1005)
* BUG FIX/ENHANCEMENT: No longer creating $0 orders when migrating MemberPress 'confirmed' subscription-confirmation transactions. #10 (@dparker1005)
* BUG FIX/ENHANCEMENT: Cleaned up the Migrate Levels step, fixing the hidden "no levels found" message and correcting the level query ordering. #12 (@dparker1005)
* BUG FIX: Fixed a query that left core PMPro pages (checkout, account, etc.) restricted after migrating "all pages"/"all content" rules. #2 (@dparker1005)
* BUG FIX: Category and tag content restrictions now migrate correctly by looking up terms by slug. #1 (@dparker1005)
* BUG FIX: Content restriction inserts now use INSERT IGNORE to avoid duplicate-key database errors on re-runs and overlapping rules. #11 (@dparker1005)
* BUG FIX: Lifetime memberships (MemberPress '0000-00-00 00:00:00') are now migrated as non-expiring instead of expired. #4 (@dparker1005)
* BUG FIX: Already-expired memberships are migrated with an 'expired' status directly, preventing a mass "Membership Expired" email blast. #3 (@dparker1005)
* BUG FIX: Migrated orders are no longer incorrectly recorded under the Stripe gateway. #5 (@dparker1005)
* BUG FIX: Existing PMPro user field groups are now preserved instead of overwritten when migrating custom fields. #7 (@dparker1005)
* BUG FIX: Migration steps no longer briefly display as completed while their queued actions are still running. #13 (@dparker1005)

= 0.1 =
* First version.
