
# SUID Checker Bash Function :computer: :lock:

![GitHub top language](https://img.shields.io/badge/language-bash-blue)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/user/repo)
![GitHub](https://img.shields.io/badge/license-MIT-green)

## Overview :mag:
This bash function, `suidcheck`, is a security tool designed to identify potentially vulnerable SUID binaries on a Unix-like system. It uses a list of known GTFO bins from [GTFOBins](https://gtfobins.github.io/), a resource listing Unix binaries that can be exploited for privilege escalation.
- I have gone through and found all SUID binaries listed on GTFO bins and now you can easily check without having to go back and forth between the standard command:

```bash
find / -perm u=s -type f 2>/dev/null
```

## Features :star:
- **Easy Integration**: Seamlessly integrates into any bash environment.
- **Comprehensive Checking**: Utilizes an extensive list of known GTFO bins.
- **Quick Detection**: Efficiently identifies SUID binaries with potential vulnerabilities.

## A fun alternative way to use this:
- This make the suidcheck directly on your clipboard ready to paste into your remote session (Make sure you do this on your host OS)
```
sudo apt-get install xclip
suidcheck=$(curl https://raw.githubusercontent.com/pentestfunctions/functions/main/suidcheck); echo $suidcheck | xclip -sel clipboard
```

## Installation :wrench:
1. Copy the `suidcheck` function code directly from github.
2. Paste it into your terminal on the remote machine.
3. The function is now available in your current shell session.

## Usage :keyboard:
Simply run the function in your terminal:
```bash
suidcheck
```

## Output :bar_chart:
- Lists vulnerable SUID binaries found on your system.
- Outputs "No SUID Priv Esc Found" if no vulnerable binaries are detected.

## Contributing :handshake:
Contributions to improve the script or extend its capabilities are welcome. Feel free to submit pull requests or open issues for suggestions and bugs.

## License :scroll:
Distributed under the MIT License. See `LICENSE` for more information.

## Acknowledgements :clap:
- Special thanks to [GTFOBins](https://gtfobins.github.io/) for providing the list of exploitable binaries.
- All contributors and users who offer feedback and suggestions.

---

Stay Secure! :shield: :key:
