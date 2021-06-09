---
layout: post
date: 2020-09-14 09:00:00
title: My MacOS Setup with Ansible
summary:
  A set of Ansible playbooks to setup, configure, and maintain my Mac. These playbooks take most of
  the effort out of configuring everything manually while keeping track of any changes.
meta_description:
  A set of Ansible playbooks to setup, configure, and maintain my Mac
categories: projects
tags: [english, cli, project, harvest, typescript]
---

<img
 src="https://raw.githubusercontent.com/flandrade/my-mac/master/media/ansible-256.png?token=ABTZYEODR7AZUVHRN5JN4US7KVV44"
  alt="Ansible logo"
  title="Ansible logo"
  style="width: 30%; min-width: 96px"
  align="right"
/>

I [published a set of Ansible playbooks][my repository] to setup, configure, and maintain my MacOS.
They set up a full local development environment with a single command, but also provide specific
commands to update more granular settings.

As a result, these playbooks take most of the effort out of installing and configuring everything
manually.

Everything needed to use and customize these playbooks is documented in
[my repository](https://github.com/flandrade/my-mac). Feel free to explore, adapt, or copy code for
your playbook!

## 📖 What you'll get?

These playbooks will do four main tasks:

- **App installations:** Command-line tools and applications installed with the fantastic [Ansible's
  Homebrew role] by Jeff Geerling. It installs and configures packages, taps, and cask apps
  according to supplied variables.

- **zsh installation:** The zsh role configures [zsh] and installs the configuration framework
  [prezto].

- **Dotfile configuration:** [This role][dotfiles role] downloads the dotfiles from my [dotfile
  repository] and it symlinks them with [Stow]. It's possible to replace this repository and use
  your own but make sure you're using [Stow]. In addition, the role also configures [vscode]: you
  can change the installed extensions by modifying the supplied variables.

- **OSX configuration:** The osx role runs a script to modify the default macOS preferences. I'm
  using the [original script] by Mathias Bynens.

## 🕹️ Credits and Inspiration

I first got the idea of starting this project from
[Sebastián Estrella's repo](https://github.com/sestrella/devbox). If you want to get started and
create your Ansible roles, check out these GitHub repositories for more inspiration:

- [Jeff Geerling’s repo](https://github.com/geerlingguy/mac-dev-playbook)
- [Adam Johnson's repo](https://github.com/adamchainz/mac-ansible)
- [Steven Loria's dotfiles](https://github.com/sloria/dotfiles)
- [Matiss Treinis's repo](https://github.com/Addvilz/dots)
- OSX [original script] by Mathias Bynens

[ansible's homebrew role]: https://galaxy.ansible.com/geerlingguy/homebrew
[zsh]: https://github.com/sorin-ionescu/prezto
[prezto]: https://github.com/sorin-ionescu/prezto
[stow]: https://www.gnu.org/software/stow/
[dotfile repository]: https://github.com/flandrade/dotfiles
[original script]: https://github.com/mathiasbynens/dotfiles
[vscode]: https://code.visualstudio.com/
[dotfiles role]: https://github.com/flandrade/my-mac/tree/master/roles/dotfiles
[my repository]: https://github.com/flandrade/my-mac
