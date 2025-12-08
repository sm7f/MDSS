# ⚙️ Zorin Tools – Setup Completo (Atualizado Zorin OS 18)

Este guia explica como configurar o **Flameshot**, **Kooha** e **All-in-One Clipboard Manager** no Zorin 18, obtendo uma experiência completa equivalente (e superior) ao Windows: copiar, capturar tela e gravar vídeos com atalhos personalizados.

---

## 🧱 0️⃣ Pré-requisito – Usar X11 (Xorg)
O Flameshot **não funciona corretamente em Wayland**, pois ele precisa de acesso direto à tela.  
Antes de configurar:

### Verifique sua sessão:
```bash
echo $XDG_SESSION_TYPE
```
- Se aparecer `x11` → perfeito.  
- Se aparecer `wayland` → altere o modo:

1. Saia da sessão (logout).  
2. Na tela de login, clique na **engrenagem ⚙️**.  
3. Escolha **“Zorin Desktop on Xorg”**.  
4. Faça login novamente.

---

## 🧠 1️⃣ All-in-One Clipboard Manager – Histórico da Área de Transferência

### Instalação
```bash
sudo apt install gnome-shell-extension-manager -y
```
Abra com:
```bash
extension-manager
```
Procure por:
```
All-in-One Clipboard Manager
```
Autor: **Maestroschan**  
Clique em **Instalar**.

### Atalho (Win + V)
1. Configurações → Teclado → Atalhos → Personalizados → **Adicionar**  
2. Nome: `Histórico da Área de Transferência`  
3. Comando:
   ```bash
   gnome-extensions prefs all-in-one-clipboard-manager@maestroschan.fr
   ```
4. Atalho: **Super + V**

---

## 🖼️ 2️⃣ Flameshot – Captura de Tela e Edição

### Instalação
```bash
sudo apt install flameshot -y
```

### Adicionar à inicialização
```bash
mkdir -p ~/.config/autostart
cp /usr/share/applications/org.flameshot.Flameshot.desktop ~/.config/autostart/
```
Isso garante que o Flameshot inicie junto com o sistema.

### Configuração no aplicativo
Clique com o **botão direito** no ícone da chama (na bandeja) → **Configurações**.

Ative:
- ✅ “Iniciar minimizado na bandeja”  
- ✅ “Permitir atalhos globais”  
- ✅ “Copiar automaticamente para a área de transferência”  
- ✅ “Mostrar barra de ferramentas após captura”

### Atalho (PrintScreen ou Super + Shift + S)
1. Configurações → Teclado → Atalhos → Personalizados → **Adicionar**  
2. Nome: `Captura de Tela (Flameshot)`  
3. Comando:
   ```bash
   flameshot gui -c
   ```
4. Atalho: **Print**  
   - Se aparecer “não é possível registrar tecla”, use **Super + Shift + S**.

### Teste manual
```bash
flameshot gui -c
```
Deve abrir o seletor de área e copiar automaticamente para o clipboard.

---

## 🎥 3️⃣ Kooha – Gravação de Tela com Áudio

### Instalação
```bash
sudo apt install kooha -y
```
ou versão mais recente:
```bash
flatpak install flathub io.github.seadve.Kooha -y
```

### Configuração
Abra **Kooha → ⚙️ Configurações** e marque:
- ✅ Gravar áudio do microfone  
- ✅ Gravar áudio do sistema  
- ✅ Mostrar cursor do mouse  
- ✅ Mostrar contador de tempo

### Atalho (Ctrl + Alt + R)
1. Configurações → Teclado → Atalhos → Personalizados → **Adicionar**  
2. Nome: `Gravar Tela`  
3. Comando: `kooha`  
4. Atalho: **Ctrl + Alt + R**

---

## ⚡ 4️⃣ Instalação Rápida (Pacote Completo)
```bash
sudo apt install flameshot kooha gnome-shell-extension-manager -y
```
Depois abra:
```bash
extension-manager
```
E instale o **All-in-One Clipboard Manager** (autor Maestroschan).

---

## 🧩 5️⃣ Atalhos Recomendados

| Função | Aplicativo | Atalho |
|--------|-------------|--------|
| Histórico de cópias | All-in-One Clipboard Manager | **Super + V** |
| Captura editável | Flameshot | **Print** *(ou Super + Shift + S)* |
| Gravação de tela | Kooha | **Ctrl + Alt + R** |

---

## ✅ 6️⃣ Teste Final

1. Pressione **Super + V** → histórico de cópias.  
2. Pressione **Print** → seletor do Flameshot (captura + edição).  
3. Pressione **Ctrl + Alt + R** → gravação de tela com o Kooha.  
4. Após reiniciar, os três apps iniciam automaticamente no Zorin 18.

---

**Feito por Herberth Amorim — Setup otimizado para Zorin OS 18.**
