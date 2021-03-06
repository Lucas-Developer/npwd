# npwd
## Command-line password management for your various accounts.

`npwd` is simple, stateless password management. You enter a master key and the name of an account (ex. "Twitter"), wait a few seconds, and npwd generates a password for that account ready in your clipboard. You can reuse the same master key for all your accounts, and npwd will generate a different password for every account. Every time you want to log in, just launch npwd and enter the same master key and account name. Simple! Useful! :rainbow: :sparkling_heart:

### Benefits
1. Memorize a single master key, but still get a different password for every account.
2. Quick and easy command-line access.
3. Copies password straight to clipboard then clears clipboard automatically in 15 seconds.
4. Doesn't store anything: no password databases to manage.

### Installation
`npm install -g npwd`

### Usage
1. `npwd`
2. Enter your master key (hidden) (same for all accounts).
3. Enter the name of your account (ex. "Twitter", "GitHub")
4. In a few seconds, your password for that account is in your clipboard.

Clipboard is cleared automatically after 15 seconds for security.

### Notes
1. Key derivation is done with scrypt. N = 2<sup>17</sup>, r = 8, p = 1, L = 16. Account name acts as salt.
2. Account names are lowercased automatically for usability. "GitHub" == "github".

### Disclaimer
npwd was written in a two-hour meeting because I was bored. No warranty, no guarantee it won't explode, summon Cthulhu, etc.
