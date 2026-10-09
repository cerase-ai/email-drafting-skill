# email-drafting-skill

A Cerase skill that gives the assistant a fixed structure and a set of rules for
drafting a professional email. The assistant uses it when the person wants a
message that will be sent as email ("write an email to…", "reply to this
email…", "send a note about…"), including when they describe the message
without saying "email". It does not apply to a reply that stays in the chat.

## What the assistant does

- Writes a subject of at most 60 characters that opens with an imperative verb
  or a concrete noun, never "Re:" or "Update".
- Builds the message as greeting, one sentence of context, one to three short
  paragraphs with one idea each, an optional call to action, and a sign-off
  with the name of the mailbox the mail leaves from: the assistant's own from
  its mailbox, the person's from theirs. Bullet lists only for more than three
  items.
- Keeps each paragraph on one line, with no manual line breaks inside it, and
  separates the blocks with a single blank line, so the recipient's mail client
  does the wrapping.
- Stays under 150 words unless a longer text was asked for, uses active
  sentences with an explicit subject, avoids "asap", "fyi" and "btw", and
  writes "by <exact date>" instead of "as soon as possible".
- When the person only asks how to phrase something, offers two versions, one
  more formal and one warmer.

The skill drafts the text; sending is up to the person or to a mail connector.

## Files

| File | Purpose |
|---|---|
| `SKILL.md` | The instructions the assistant loads: `name` and `description` frontmatter, then the structure and rules. |
| `cerase.json` | Marketplace manifest: namespace `studio.guidance`, name `email-drafting`, display name, description, licence. |
| `LICENSE` | MIT licence text. |

## Installation

Published in the Cerase Marketplace as `studio.guidance/email-drafting`
([marketplace page](https://marketplace.cerase.ai/en/p/studio.guidance/email-drafting)).
A Cerase appliance also ships it in its image and attaches it to every
assistant; an administrator cannot detach it.

## License

MIT. See [LICENSE](LICENSE).
