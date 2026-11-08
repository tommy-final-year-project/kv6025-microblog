# KV6025 Microblog Design Notes

These notes record suggestions from the project conversation on 8 November 2026. They are planning notes for Part 1. The proposed theme, name and follow-up feature are open for review.

## Recommended topic

**Game walkthrough tips**, with **NextTry** as a working name. Focus each text post on one point where a player gets stuck and one action they can try on the next attempt. Short text fits this task because a player can scan a tip and return to the game quickly. Food sharing and travel guides were also considered. Their posts often benefit from photos, addresses and maps.

Example post: “During the boss’s second phase, dodge the first two swings. Wait for the third swing to finish before attacking.”

## Suggested user flow

1. Open a timeline of public text posts in chronological order, newest first.
2. Search or filter by game and encounter to find a short tip.
3. Open the tip. If the author has shared a follow-up, use the link to read the updated strategy.

The coursework core also includes account registration, sign-in and sign-out, plus creating, editing and deleting your own text posts. Game and encounter filters are proposed features.

## Optional follow-up feature

The earlier **Stuck → Solved** idea can be adapted to game tips. If the author discovers a more reliable tactic later, they can publish it as a separate post and link it to the original. The original keeps its context, and the new post appears in the timeline at its own publication time.

For a first version, allow at most one follow-up per original post, created by the original author. A possible implementation is an optional reference to the original post on the follow-up. If the follow-up is deleted, remove the update link from the original. Decide whether to include this feature after the coursework core works.

An ordinary edit, such as fixing a typo, can show an **Edited** label and keep the original publication time. Check post ownership in the PHP API before accepting edits or deletions. Test this with two accounts, including an attempt to edit a post using the other account and the post ID.

## Part 1 planning

- **App Design:** Show the timeline, finding a tip by game or encounter, and the post detail. If the follow-up is in scope, show the original and linked update. Include the account and post management mockups needed to explain the core flows.
- **Technical Overview:** Draw a small architecture diagram for React and Vite, the PHP API and MariaDB. Show how an edit moves through the three layers. Keep the ERD centred on users and posts. Add game, encounter or follow-up relationships once those design choices are confirmed.
- **Development Approach:** Verify the NUwebspace deployment and Chrome PWA installation early. Implement account access, the timeline and owner-only post actions before adding filters and follow-ups. Use GitHub issues for acceptance criteria, review Cursor changes and test the result before pushing.

## Earlier concept

Unibble was an earlier campus microblog example for planning Part 1. Its campus-specific features were discussed separately from the NextTry proposal.
