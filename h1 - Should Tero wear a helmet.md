# h1 Should Tero wear a helmet? 

## Threat modeling

### Braiterman et al 2020

- Threat modeling means examining all the ways our systems could be compromised and determining how to prevent or protect against these risks before they occur.
- The threat modeling manifesto acts as a guide for creating or improving a threat modeling method that meets the organization’s needs.
- Key questions of threat modeling are:
  1. What are we working on?
  2. What can go wrong?
  3. What are we going to do about it?
  4. Did we do a good enough job?

### Shostack 2022

- STRIDE categorises risks into: Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service and Elevation of Privileges.
- Risk management and threat modeling go together. Risk management calculates the likelihood and effect of a threat. It helps to determine the best actions to take regarding a threat, but we must do threat modeling first.

### OWASP CheatSheets Series Team 2021

- Threat modeling should be done early in the software development life cycle.
- Threat modeling is usually a team effort where members are encouraged to share ideas and give feedback to one another.

## Infosec scene

### Darknet Diaries Ep. 136: Team Xecuter

- Main topic of the episode is about modding consoles and how companies are trying to prevent that.
- This episode focused on Team Xecuter, a hacking group.
- They interviewed Gary Bowser, a key figure in the mod chip and console hacking scene.
- Gary had a career in developing software and hardware.
- He transitioned into repairing and modifying consoles like the PS1 and Xbox. He was fascinated by their restricted design when compared to early computers.
- Gary worked with MAXiMiLiEN, who was a piracy group leader and later became a mod chip businessman. Together, they promoted and sold tools like the SX Pro, which allowed people to hack the Nintendo Switch.
- Nintendo and Sony started to enforce anti-modding measures.
- Gary was later arrested by the FBI.
- Even in the current day, Nintendo aggressively protects its IP with them sending cease and desist letters and threatening legal action to cancel Super Smash Bros. Melee tournaments to seemingly protect their brand.

## a) Security hygiene

- Use strong, unique passwords. Avoid common passwords and do not reuse them. Use a mix of characters, numbers, and symbols. Use a password manager. 
- Avoid sensitive transactions on public Wi-Fi or use a VPN for encryption.
- Enable multi-factor authentication.
- Use antivirus. Regularly scan your devices for malware and viruses.
- Update software if there is an update available. Keep your operating systems, apps, and antivirus software up to date for security updates.
- Be wary of phishing scams. Avoid clicking links from unknown sources.
- Don't share private info on the internet. Be especially careful not to overshare on social media.
- Back up important data. Use external drives for backups.
- Wipe personal data before giving or selling old devices.

## b) Make-belief boogie-man

Big gaming company named MK Games.

### What are we working on?
   - Due to being a big gaming company we have a lot of customers and data.
   - Reputation is really important so security measures must be good to keep paying customers/playerbase.

### What can go wrong?
   - Hackers are targeting us as we're a big gaming company and have lots of data which they can use to get money.
   - Hackers might try a DDoS attack to cause harm to the company especially during holiday seasons when most people are home. This would lead to people not being able to play our games and causing massive harm in reputation.
   - In case of customers who pre-order games, hackers might try to access game files before the game is released and leak the files to the public. This could possibly cause customers to get disappointed if the game is not like they expected it to be which can lead to customers cancelling their pre-orders and so, company loses money.
   - Specifically applying STRIDE:
      - Spoofing
        - Hackers pretending to be admin to gain access.
      - Tampering
        - Hackers leak game files that aren't supposed to be public.
      - Repudiation
        - Hackers deny their action to escape consequences
      - Information Disclosure
        - Hackers steal customer data or leak unreleased game content to public.
      - Denial of Service
        - DDoS attacks that overwhelm game servers and making games unplayable during peak times.
      - Elevation of Privileges
        - Hackers take advantage of weaknesses to increase their permissions to look at files that they shouldn't be able to see.

### What are we going to do about it?
- Use META model (Mitigate, Eliminate, Transfer, Accept) to increase security.
- Implement DDoS protection services to detect and block attacks before they affect players.
- Use encryption and multi-factor authentication to protect sensitive customer data and game files. This helps to stop unauthorized access.
- Educate employees on security awareness (for example not to click on links on emails unless it's authorized).
- Making sure all systems are up to date with security measures.
- Something we have to accept is that no system is 100% safe.
 
### Did we do a good enough job?
Security must always be improved as new methods to breach will be found so while we might have done a good job for now, it won't be enough in the future.

## References

- Armer Michael, 4 Ways to Always Be Improving Security. The Enterprisers Project, 2020, https://www.enterprisersproject.com/article/2020/6/security-4-tips-constant-improvement.
- Israel Aliza, It’s Christmas for the Hackers, Too! DDoS in the Holiday Season. MazeBolt Blog 2024, https://www.mazebolt.com/blog/its-christmas-for-the-hackers-too-ddos-in-the-holiday-season.
- Karvinen 2024: Information Security Course, https://terokarvinen.com/information-security/
- "Modding Your Switch Can Land You In Prison - Darknet Diaries Ep. 136: Team Xecuter" Youtube - Darknet Diaries, Jack Rhysider, https://www.youtube.com/watch?v=E0ihjLKM0QI
- OWASP CheatSheets Series Team 2021, https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html
- Threat Modeling Manifesto, https://www.threatmodelingmanifesto.org/
- World's Shortest Threat Modeling Course, Youtube, Adam Shostack, https://www.youtube.com/playlist?list=PLCVhBqLDKoOOZqKt74QI4pbDUnXSQo0nf
