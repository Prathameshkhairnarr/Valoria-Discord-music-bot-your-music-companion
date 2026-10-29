# Valoria Privacy Policy

Effective date: 29 October 2026

**Operator:** Vicky Khairnar  
**Contact:** devsvicky0@gmail.com

This policy describes the Valoria Discord music bot and its current features. Valoria is independently operated and is not affiliated with Discord or the music providers it accesses.

## 1. What Valoria processes

Valoria processes commands, selected music-provider metadata, Discord user/server/channel identifiers, relevant permissions and voice-channel membership to provide music playback and related features. It does not record voice conversations or subscribe to incoming voice audio.

Slash commands and bot-mention commands are supported. When Message Content Intent is enabled, custom-prefix commands and owner-authorized no-prefix commands are also supported. The bot can receive message content permitted by Discord's intent rules, but only handles addressed, prefixed or recognized authorized commands. It does not retain unrelated conversations or raw command messages in its database. It does not use Discord message content to train AI models.

## 2. Stored data and purposes

- **Server settings:** server IDs, DJ role IDs, preferred catalog, prefix, language, volume, 24/7/autoplay preferences, appearance, channel restrictions and configured player channel/message IDs.
- **Saved playlists:** user ID, playlist name, creation time, public-sharing state, song order, provider track IDs and track titles. Private playlists are not accessible to other listeners through the bot. Shared playlists intentionally expose their owner ID, name and track metadata.
- **Profiles:** user ID and optional user-written bio. Profiles may display the user's Discord avatar, account creation date, access badges, playlist counts and server premium state. Bios are intended to be public; do not include private information. A different user requesting your profile does not receive your personal music-taste summary; your own text-command profile response can still be visible in the channel.
- **No-prefix access:** authorized user IDs and the granting owner's ID. Access records allow the operator to manage who can run commands without a prefix.
- **Music preferences:** when enabled, user/server IDs, track metadata, approximate listening duration, play/skip counts and preference weights for musical moods, artists, language and energy. These are used for the requested personalization feature, not advertising or unrelated profiling. Musical moods are approximate song descriptions, not diagnoses or assessments of a person's emotional or mental health. Current Spotify-linked tracks are excluded from personal preference learning.
- **Recent server music history:** up to 120 metadata snapshots per server, including provider IDs/titles and available artist/language metadata, to reduce autoplay repetition. These records do not include requester IDs or names.
- **Premium access:** code hashes, validity periods, redemption times, redeemed server IDs and server entitlement expiry. Raw redeem codes are not stored in this ledger. The current Buy Now button does not process payments.

The bot does not store audio files, signed audio-stream URLs, Discord passwords or user login tokens in its database. Bot and provider credentials are operational secrets and must not be submitted through support requests.

## 3. Temporary data and Discord messages

Process memory can contain current/upcoming track metadata, requester display names and IDs, stream URLs, encoded playback metadata, voice-session credentials needed for playback, votes, cooldowns, search selections and bounded artwork/metadata caches. These are cleared or replaced as features end, caches expire/are evicted, or the process stops. Cache expiration does not promise immediate physical erasure from memory.

Player cards, command responses and user-supplied profile text can be sent to Discord. Message-command replies are visible in the channel; most slash-command acknowledgments are private, while the shared player is visible to channel members. Discord and server moderators control Discord-message retention. Database deletion does not retract all previously sent Discord messages or already shared information.

## 4. Providers and hosting

Song queries, public track identifiers and playback requests are sent to the selected or matching providers, which can include YouTube/YouTube Music, SoundCloud, Spotify, Apple/iTunes, Deezer, Audius and Jamendo. Spotify and Apple catalogs identify music; current full playback uses a matching YouTube recording, not native Spotify/Apple streaming. Providers receive the playback host's network address and requested metadata. Valoria does not attach a listener's Discord user ID to provider searches.

Lavalink processes track requests and Discord connection information needed to deliver audio, including bot, server/channel and voice-session identifiers. Discord processes interactions and audio under its own policies. The hosting operator can process application files, database storage, network traffic and console output under its own terms.

Valoria can check Altare's public hosting-status feed after sustained playback stalls. These requests contain no song queries, listener IDs or bot credentials; the status service receives the bot host's network address. In-memory incident records include affected channel/message references and configured hosting component IDs and expire within 24 hours or process shutdown.

Following the optional lyrics-search link sends its query to the lyrics website. Contacting support by email causes the email provider and operator to receive the information you choose to send. Each provider has its own privacy practices. Valoria does not sell personal data or use it for targeted advertising.

## 5. Retention and deletion

- Server settings remain until an authorized manager uses `/deletedata scope:guild` or removes the bot. This also clears that server's preference profiles and recent-history records.
- Saved playlists and bios remain until edited/deleted or `/deletedata scope:user` is used. User deletion clears saved playlists, bio, granted no-prefix access and stored personal music preferences across the bot's servers. Host-configured bot-owner identity remains an operator setting.
- Personal preference profiles are bounded to 100 track metadata records and 200 preference weights and expire after 90 days of inactivity. Expired records are pruned on startup/subsequent activity, not at a guaranteed instant while offline.
- Recent server history is limited to 120 records per server and a seven-day usable window. Expired records are ignored on reads and pruned during initialization/history writes.
- Premium redemption/entitlement records are separate from ordinary server settings and are not erased by the settings-reset command. For deletion of these records, contact the operator; removing an entitlement can end premium access. Used-code records may be retained without unnecessary identifiers to prevent reuse where implemented.
- Operational console logs may contain controlled event names, public track titles/IDs, timing, aggregate counts and technical connection state. Valoria does not itself run a persistent log archive or automatic backup scheduler. Host-managed console history, backups and operator-created snapshots have separate retention controls; deletion from the active database does not immediately erase those copies. Contact the operator to request their review and removal where available.

To request access, correction, restriction or deletion beyond the available commands, email **devsvicky0@gmail.com**. Include only the relevant Discord user/server ID and request details. We may verify control of that account/server before disclosing or deleting data. Do not send passwords, bot tokens, identity documents or payment details by email or Discord messages to the bot. Requests will be handled subject to applicable law and necessary security/entitlement checks.

## 6. Security, age and policy changes

Valoria uses application access checks, parameterized database operations and restricted handling of credentials. The current deployment uses SQLite storage without application-level database encryption. Encryption at rest for hosting volumes and backups has not been independently confirmed; we do not claim that this protection is currently in place. No service can guarantee absolute security. Security concerns can be reported to the contact above. Where required, the operator will notify Discord and affected users about unauthorized access.

Use is limited to people eligible to use Discord under its age requirements and applicable local law. Valoria does not intentionally solicit sensitive personal information. This policy may change with the service; material changes will be reflected in the published policy and its effective date. Contact the operator with questions.
