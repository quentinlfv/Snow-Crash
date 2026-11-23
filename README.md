
# SnowCrash

## About the Project

SnowCrash is a cybersecurity project from the 42 curriculum designed to introduce fundamental security concepts through a series of practical CTF challenges.

The objective is to explore and exploit vulnerabilities in a controlled Linux environment, progressively developing an understanding of system security, privilege management, binary analysis, and common exploitation techniques.

Each level presents a specific challenge that requires investigating the environment, understanding the underlying mechanisms, identifying security weaknesses, and finding a way to retrieve the associated flag.

## Retrieving the Flag

Each level is completed by exploiting the identified vulnerability to gain access to the corresponding user account.

Once the required privileges have been obtained, the flag can be retrieved by executing the following command with the right permissions:

```bash
getflag
```

## Learning Objectives

Throughout this project, we explore several cybersecurity concepts, including:

- **Linux System Administration:** File permissions, SUID binaries, environment variables, processes, and scheduled tasks.
- **Privilege Escalation:** Identifying and exploiting misconfigured permissions and privileged executables.
- **Binary Analysis:** Inspecting executables using tools such as `strings`, `objdump`, `readelf`, and GDB.
- **Reverse Engineering:** Understanding program behavior through disassembly and low-level analysis.
- **Web Security:** Exploring vulnerabilities involving PHP, CGI, and command injection.
- **Shell Exploitation:** Understanding command injection, environment manipulation, and symbolic links.
- **Dynamic Linking:** Investigating shared libraries, `LD_PRELOAD`, and related security mechanisms.

## Project Structure

Each directory corresponds to a level and contains the relevant resources, investigation notes, and exploitation techniques used to solve the challenge.

```text
SnowCrash/
├── level00/
├── level01/
├── level02/
├── ...
├── level09/
└── README.md
```

## Methodology

For each level, the approach follows a structured investigation process:

1. **Reconnaissance:** Inspect the available files, permissions, and system configuration.
2. **Analysis:** Examine scripts and executables to understand their behavior.
3. **Vulnerability Identification:** Determine which security weaknesses can be exploited.
4. **Exploitation:** Develop and test an approach to retrieve the flag.
5. **Documentation:** Record the investigation process, commands, and relevant technical concepts.

## Environment & Tools

The project is carried out in a Linux environment using various system and debugging utilities:

- Linux / Unix
- Bash
- GDB
- `strings`
- `objdump`
- `readelf`
- `hexdump`
- `strace`
- `ltrace`
- SSH

## Disclaimer

This repository documents solutions to educational cybersecurity challenges provided as part of the 42 curriculum.

All techniques are explored exclusively within the SnowCrash training environment and are intended for educational purposes.
