---
name: league-of-legends-coach
description: "Coach a League of Legends player. Read your OP.GG profile and recent games, then get three habits to fix, champion advice and a matchup plan. Works through ApexGenius with a connected OP.GG account; load it from any compatible AI agent."
metadata:
  category: games
  source: "ApexGenius shipped skill OPGGLeagueCoach 1.0.0"
---

# Coach a League of Legends player from OP.GG stats

## Try asking

> Look up my Riot ID on OP.GG and coach me: my champion pool, the habits costing me games, and how to play my next lane matchup.

## What this needs

The player's Riot ID (game name and tag) and region, their main role, and the champion or matchup they want help with, if any.

## Use the connected app

Use the user's enabled OP.GG connection. It reads public data from OP.GG's official MCP; no OP.GG sign-in, Riot password, or API key is needed. Discover `opgg_search_tools` with `apex_search_tools`, call it through `apex_call_read_tool` for each step below, then call `opgg_call_read_tool` with the exact `remote_tool_name` and `arguments` it returns. Only reviewed reads are allowed, so nothing in the player's account changes and no undo is needed. Report the connector as partially ready if its first read has not been checked.

## 1. Read the profile

Use `lol_get_summoner_profile` for the Riot ID and region: rank, recent form, and champion pool. If the ID is not found, ask for the exact game name, tag, and region instead of guessing a similar player.

## 2. Read recent games

Use `lol_list_summoner_matches` for the last 20 games. Count wins and losses by champion and role, and note games far from the player's usual role.

## 3. Look closely at a few games

Pick two or three recent losses on the player's main champion and read each with `lol_get_summoner_game_detail`. Compare deaths, farm, vision, and damage with the lane opponent. Look for the same pattern across games, not one bad game.

## 4. Compare with the meta

Use `lol_get_champion_analysis` and `lol_list_lane_meta_champions` for the player's champions and role: builds, win rates, and pick rates in their tier. Use `lol_get_lane_matchup_guide` for the matchup they asked about.

## 5. Coach

Give three habits to change, each with the games that show it. Say which champions to keep, drop, or add, and why. Give one build and one plan for the next matchup.

## Deliverable

A short coaching note: rank and form, three habits with match evidence, champion pool advice, and the matchup plan, with OP.GG named as the source and the time the data was read.

## Verify the result

State the region, the number of games read, and the patch the stats come from. Stats change every patch, so date the advice.

## If something fails

If a read fails or returns nothing, say which step and keep the rest of the note to what was read. An empty match list is not proof the player has not played. Do not invent statistics.

## Source and adaptation

[Provider source](https://github.com/opgginc/opgg-mcp). Publisher: OP.GG. ApexGenius authored this outcome-specific procedure using the provider reference and the gateway tool schemas. It includes a defined input, ordered procedure, output contract, and readback/recovery checks. This is an ApexGenius adaptation, not a claim that the provider certified the workflow or that every external effect has been exercised.
