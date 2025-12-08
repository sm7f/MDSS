# 🎯 Ferramentas de Produtividade no Zorin OS 18

Este guia explica como configurar o **Kooha**, **Ksnip** e **All-in-One Clipboard Manager**, obtendo uma experiência completa equivalente (e superior) ao Windows: copiar, capturar tela e gravar vídeos com atalhos personalizados.

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

## 🖼️ 2️⃣ Ksnip – Captura de Tela e Edição

### Instalação
```bash
sudo apt install ksnip -y
```
### Atalho (PrintScreen)
1. Configurações → Teclado → Atalhos → Personalizados → **Adicionar**  
2. Nome: `Captura com Ksnip`  
3. Comando: `ksnip`  
4. Atalho: **Print**

### Dica
No **Ksnip → Configurações → Captura**, marque:
- Copiar automaticamente para área de transferência  
- Fechar automaticamente após capturar (opcional)

---

## 🎥 3️⃣ Kooha – Gravação de Tela com Áudio

### Instalação
```bash
sudo apt install kooha -y
```
ou a versão mais recente:
```bash
flatpak install flathub io.github.seadve.Kooha -y
```

### Configuração
Abra **Kooha → ⚙️ Configurações** e marque:
- Gravar áudio do microfone  
- Gravar áudio do sistema  
- Mostrar cursor do mouse  
- Mostrar contador de tempo  

### Atalho (Ctrl + Alt + R)
1. Configurações → Teclado → Atalhos → Personalizados → **Adicionar**  
2. Nome: `Gravar Tela`  
3. Comando: `kooha`  
4. Atalho: **Ctrl + Alt + R**

---

## ⚡ 4️⃣ Pacote Completo (Instalação Rápida)
```bash
sudo apt install kooha ksnip gnome-shell-extension-manager -y
```

Depois abra:
```bash
extension-manager
```
e instale o **All-in-One Clipboard Manager** (autor Maestroschan).

---

## 🧩 Atalhos Recomendados

| Função | Aplicativo | Atalho |
|--------|-------------|--------|
| Histórico de cópias | All-in-One Clipboard Manager | **Super + V** |
| Printscreen editável | Ksnip | **Print** |
| Gravação de tela | Kooha | **Ctrl + Alt + R** |

---

Feito por Herberth Amorim – Setup otimizado para Zorin OS 18.
