# openhook APT Repository

APT repository for installing the [openhook CLI](https://github.com/openhook-dev/openhook-cli) on Debian/Ubuntu systems.

## Installation

### Quick install

```bash
curl -fsSL https://openhook-dev.github.io/apt/gpg.key | sudo gpg --dearmor -o /usr/share/keyrings/openhook.gpg
echo "deb [signed-by=/usr/share/keyrings/openhook.gpg] https://openhook-dev.github.io/apt stable main" | sudo tee /etc/apt/sources.list.d/openhook.list
sudo apt update
sudo apt install openhook
```

### Step by step

1. Download and install the GPG key:
```bash
curl -fsSL https://openhook-dev.github.io/apt/gpg.key | sudo gpg --dearmor -o /usr/share/keyrings/openhook.gpg
```

2. Add the repository:
```bash
echo "deb [signed-by=/usr/share/keyrings/openhook.gpg] https://openhook-dev.github.io/apt stable main" | sudo tee /etc/apt/sources.list.d/openhook.list
```

3. Update and install:
```bash
sudo apt update
sudo apt install openhook
```

## Updates

Once installed, openhook will be updated with your regular system updates:

```bash
sudo apt update
sudo apt upgrade openhook
```

## Uninstall

```bash
sudo apt remove openhook
sudo rm /etc/apt/sources.list.d/openhook.list
sudo rm /usr/share/keyrings/openhook.gpg
```

## Links

- [openhook CLI](https://github.com/openhook-dev/openhook-cli)
- [openhook website](https://openhook.dev)
