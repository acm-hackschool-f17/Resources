# Hackschool Learn Session 4: Relational Databases

**Location**: Covel 227

**Time:** 6:15 - 8:15

**Teachers:**

- Shannon Phu

**Slides:**

- [Session 4 - Relational Databases]\(TBD)

**Cheat Sheets:**

- TBD

**Course Overview Table of Contents**:

- [Course Schedule](https://github.com/acm-hackschool-f17/Resources/blob/master/README.md#basic-curriculum)

**Mentor Voting Form**:

- [Mentor Voting Form]\(TBD)

**Attendance Code:** TBD

## What we'll be learning today

- TBD

## What is Docker?

Docker is a tool that allows developers, sys-admins etc. to easily deploy their applications in a sandbox (called **containers**) to run on the host operating system, i.e. Linux. 

The key benefit of Docker is that it allows users to **package an application with all of its dependencies into a standardized unit** for software development. 

Unlike virtual machines, containers do not have the high overhead and hence enable more efficient usage of the underlying system and resources.

### What are containers?

The industry standard today is to use **Virtual Machines** (VMs) to run software applications. A VM simulates an operating system; it's kind of like a computer running as software inside another computer.

VMs are great at providing full process isolation for applications: there are very few ways a problem in the host operating system can affect the software running in the guest operating system, and vice-versa. But this isolation comes at great cost — the computational overhead spent virtualizing hardware for a guest OS to use is substantial.

Containers take a different approach: by leveraging the low-level mechanics of the host operating system, containers provide most of the isolation of virtual machines at a fraction of the computing power.

### Installing Docker

**On Mac:**

Click [here](https://www.docker.com/community-edition#/mac) and follow the instructions to download Docker.

**On Windows:**

Click [here](https://store.docker.com/editions/community/docker-ce-desktop-windows) and follow the instructions to download Docker.

#### Once Docker is installed:

Run Docker, then use your Terminal/Command Prompt to see if everything's set up. 

**On both Linux/Mac and Windows:**

```
$ docker version
```

This should output:

```
Client:
 Version:      17.09.0-ce
 API version:  1.32
 Go version:   go1.8.3
 Git commit:   afdb6d4
 Built:        Tue Sep 26 22:40:09 2017
 OS/Arch:      darwin/amd64

Server:
 Version:      17.09.0-ce
 API version:  1.32 (minimum version 1.12)
 Go version:   go1.8.3
 Git commit:   afdb6d4
 Built:        Tue Sep 26 22:45:38 2017
 OS/Arch:      linux/amd64
 Experimental: true
```

All set!