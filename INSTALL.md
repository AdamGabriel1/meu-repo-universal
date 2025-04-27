# Instalação do Repositório

#### Arch Linux
```bash
sudo tee -a /etc/pacman.conf << EOF
[meu-repo-arch]
SigLevel = Optional TrustAll
Server = https://seu-usuario.github.io/meu-repo-universal/arch/\$arch
EOF

sudo pacman -Syu
```

#### Debian/Ubuntu
```bash
echo "deb [trusted=yes] https://seu-usuario.github.io/meu-repo-universal/debian/ stable main" | sudo tee /etc/apt/sources.list.d/meu-repo.list
sudo apt update
```

#### Fedora
```bash
sudo tee /etc/yum.repos.d/meu-repo.repo << EOF
[meu-repo-fedora]
name=Meu Repositório Fedora
baseurl=https://seu-usuario.github.io/meu-repo-universal/fedora/
enabled=1
gpgcheck=0
EOF

sudo dnf update
```
