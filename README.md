# Hype Arcade 🕹️

A neon arcade high score board for employee advocacy.

Your team logs every LinkedIn and Instagram play (posts, reshares, comments, likes, stories). Each play scores points, the board ranks everyone, and the top player wins the prize.

![Hype Arcade preview](preview.jpg)

**Try the demo:** https://alyssanewman.github.io/hype-arcade/

Built with Claude by Alyssa Newman, [PVLP Social](https://pvlpsocial.com).

---

## What's inside

- Glowing neon bubble letters, a synthwave grid floor and CRT scanlines
- High scores with neon 1ST / 2ND / 3RD badges
- Log a play: pick LinkedIn or Instagram, pick the move, paste the link
- A rules panel that builds itself from your point values
- A live feed of the latest plays
- A Game Master panel for contest dates and removing fake plays
- A daily like cap (10 by default) so nobody farms likes
- The same post can't score twice for the same move

## Two ways to run it

| | Demo mode | Team mode |
|---|---|---|
| Where | GitHub Pages, or open `index.html` on your computer | Published as a Claude artifact |
| Who sees the scores | Only the person on that browser | Everyone you share it with |
| Good for | Showing people, testing your setup | Running a real contest |

The page detects where it's running. On GitHub it opens in demo mode with five sample players. Inside Claude it switches to one shared, live board for the whole team.

## Make your own with Claude (about 5 minutes)

1. Open the [live demo](https://alyssanewman.github.io/hype-arcade/#makeOwn) and scroll to **Make Your Own**.
2. Click **Download** to save the board, then **Copy Prompt**.
3. Click **Open Claude**, attach the file and paste the prompt.
4. Answer Claude's questions (company name, prize, dates).
5. Claude publishes your board. Share the link with your team.

Prefer to do it by hand? Download `index.html` from this repo and use the prompt in [MAKE-YOUR-OWN.md](MAKE-YOUR-OWN.md).

Teammates need a claude.ai account to play on the shared board.

## Customize it by hand

Everything lives in the `CONFIG` block at the top of the script in `index.html`:

```js
const CONFIG = {
  company: "Your Company",
  instagram: "@yourcompany",
  titleLines: ["HYPE", "ARCADE"],
  prize: "$100",
  likeCap: 10,
  moves: [ /* point values for every play */ ],
};
```

Change the words, the prize, the point values or the plays. The rules panel updates to match.

## Put your own copy on GitHub Pages

1. Click **Use this template** at the top of this repo, then **Create a new repository**.
2. In your new repo, open **Settings → Pages**.
3. Under **Branch**, pick `main` and `/ (root)`, then **Save**.
4. Wait a minute. Your board is live at `https://<your-username>.github.io/<repo-name>/`.

## License

MIT. Use it, remix it, run a contest with it. A shout-out is always appreciated.
