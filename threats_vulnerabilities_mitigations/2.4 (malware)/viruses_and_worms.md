# Viruses

Viruses are malware that can reproduce itself. When you execute a program, it infects your computer and spreads to other files on your computer **or** other devices on a network, like a sickness (virus) does with people.

While most of them cause some form of problems, some are just invisible and annoying. They might just exist in the background, take up space, or just be spammed in the anti-virus.

## Types of viruses

- Program
  - Part of an application, will run when application is executed
- Boot Sector
  - Boots with the OS, practically automatically
- Script viruses
  - Operating system and browser based, relatively simple
- **Fileless virus**
  - These are stealthy and because they're not a file, they usually avoid anti-virus.
  - They usually happen in the memory of your system, not a drive.
    - This usually is caused by exploits via Java/Windows that allows a script to launch and run scripts in PowerShell. This alone can be catastrophic for a computer.

# Worms

Worms are a virus, but are a lot more big of a deal. These self replicate; they do not need you to do anything, there are typically ways (exploited applications, backdoors, etc) that uses the network as a medium. It happens fast and can take over systems very quickly. **WannaCry** was, unfortunately, a worm.

Firewalls or IDS can help mitigate worms, but often times there is not much help from these if the worms actually get inside. 