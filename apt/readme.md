## apt(Advanced Package Tool)

apt is the default package manager for debian-based linux distributions(like ubuntu).
It is used to install, update, upgrade, remove, and manager software packages.
apt fetches packages from online repositories and handles dependencies automatically.

### Why is apt required?

1. Manages software easily -> No need to download files manually.
2. Handles Dependencies -> Installs required libraries automatically.
3. Keeps System Updated -> Allows easy updates and upgrades.
4. Secure -> Downloads from trusted sources.

### Common commands

1. Update package list

> sudo apt update

2. Upgrade install packages

> sudo apt upgrade

3. Install a package

> sudo apt install package-name

4. Remove a package

> sudo apt remove package-name

5. Remove package + config files

> sudo apt purge package-name

6. Show package details

> apt show package-name

7. List installed packages

> apt list --installed

8. Clean up unused packages

> sudo apt autoremove

9. Clean package cache

> sudo apt clean
