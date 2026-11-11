# Make your own Hype Arcade with Claude

Easiest way: open the [live demo](https://alyssanewman.github.io/hype-arcade/#makeOwn) and use the **Make Your Own** buttons to download the board and copy this prompt.

Or do it by hand: attach `index.html` to a new chat at [claude.ai](https://claude.ai), then copy and paste everything in the box below.

```
I'm attaching the Hype Arcade HTML file. It's "Hype Arcade," a neon arcade-style
employee advocacy leaderboard. My team logs LinkedIn and Instagram plays
and competes for a prize.

Please make it mine:

1. Ask me these questions first, all at once:
   - Company name and Instagram handle
   - The two short words for the big bubble-letter title (or keep HYPE ARCADE)
   - The prize
   - Contest start and end dates
   - Who runs the contest (the name teammates should ask for access)
   - Any point values or plays I want to change

2. Edit only the CONFIG block at the top of the script. Keep the design,
   the scoring logic and the storage code as they are.

3. Publish it as an artifact with these capabilities, so my whole team shares
   one live leaderboard:

   {
     "db": {
       "rules": [
         { "path": "players", "read": "view", "write": "admin" },
         { "path": "players/{self}", "read": "view", "write": "interact" },
         { "path": "config", "read": "view", "write": "admin" }
       ]
     },
     "user": { "scopes": ["profile"] }
   }

4. Write my contest dates to the config/season document as
   { startsAt, endsAt } in milliseconds (start at 12:00 AM, end at 11:59 PM
   my local time).

5. Tell me how to share it so teammates can log plays.
```

## What happens next

- Claude asks its questions, updates the file and publishes your board.
- You get a private link. Share it with your team and give them access to interact with it.
- Each teammate signs in, enters their initials and starts logging plays.
- As the owner, you see the Game Master panel. Use it to change dates or remove a fake play.

## Tips for a good contest

- Run it for two to four weeks. Shorter keeps energy high.
- Post a screenshot of the top three every Friday.
- Give the prize in public. It's the best ad for the next round.
