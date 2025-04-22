# Instalação do Repositório

## 1. Importar a Chave GPG
```bash
curl -sL https://AdamGabriel1.github.io/packages/x86_64/meu-repo-public-key.gpg | sudo pacman-key --add -
sudo pacman-key --lsign-key CF4CCDE1CA5F144B86C8503637520F5A32155660
```

## 2. Adicionar o Repositório
```bash
echo '[meu-repo]
SigLevel = Required DatabaseOptional TrustedOnly
Server = https://AdamGabriel1.github.io/packages/$arch' | sudo tee -a /etc/pacman.conf

sudo pacman -Syu
```
