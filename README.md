# 🧩 README — Zorin Tools Setup v2

## ⚙️ Projeto
**Zorin Tools Setup v2** é um guia completo e automatizado criado por **Herberth Amorim**, projetado para otimizar o ambiente do **Zorin OS 18**, tornando-o uma alternativa produtiva, estável e poderosa ao Windows.

Ele reúne as melhores ferramentas de captura, gravação e produtividade, com foco em eficiência para desenvolvedores, testadores QA e usuários avançados.

---

## 🚀 Recursos Principais

| Função | Ferramenta | Descrição |
|--------|-------------|-----------|
| 📋 Histórico de Cópias | **All-in-One Clipboard Manager** | Gerencia todo o histórico de Ctrl+C com atalho **Super + V** |
| 🖼️ Captura de Tela | **Flameshot** | Captura, edita e copia imagens rapidamente (**Print** / **Super + Shift + S**) |
| 🎥 Gravação de Tela | **Kooha** | Grava tela com áudio e contador, estilo OBS simplificado (**Ctrl + Alt + R**) |

---

## 🧱 Pré-requisito

O setup funciona **apenas em sessão X11 (Xorg)**, pois o Flameshot e o Kooha não têm suporte total a **Wayland**.

Verifique seu ambiente atual:
```bash
echo $XDG_SESSION_TYPE
```
Se retornar `wayland`, altere para:
1. Logout da sessão  
2. Na tela de login, clique na **engrenagem ⚙️**  
3. Selecione **Zorin Desktop on Xorg**  
4. Faça login novamente  

---

## 🧠 Instalação Rápida
```bash
sudo apt update
sudo apt install flameshot kooha gnome-shell-extension-manager -y
```
Depois abra:
```bash
extension-manager
```
E instale **All-in-One Clipboard Manager (autor: Maestroschan)**.

---

## 🧩 Atalhos Recomendados

| Função | Aplicativo | Atalho |
|--------|-------------|--------|
| Histórico da área de transferência | All-in-One Clipboard Manager | **Super + V** |
| Captura editável | Flameshot | **Print** *(ou Super + Shift + S)* |
| Gravação de tela | Kooha | **Ctrl + Alt + R** |

---

## 🔧 Configurações Extras

### Flameshot
```bash
mkdir -p ~/.config/autostart
cp /usr/share/applications/org.flameshot.Flameshot.desktop ~/.config/autostart/
```
Ativar nas Configurações:
- Iniciar minimizado na bandeja  
- Permitir atalhos globais  
- Copiar automaticamente para a área de transferência  
- Mostrar barra de ferramentas após captura  

### Kooha
Ativar nas Configurações:
- Gravar áudio do sistema e microfone  
- Mostrar cursor e contador de tempo  

---

## 🧪 Testes
- `Super + V` → histórico de cópias  
- `Print` → seletor do Flameshot  
- `Ctrl + Alt + R` → gravação com Kooha  

Após reiniciar, todos os aplicativos iniciam automaticamente.

---

## 🧑‍💻 Autor
**Herberth Amorim**  
Desenvolvedor | Analista de Requisitos | Pentester  
💼 GitHub: [sm7f](https://github.com/sm7f)

---

## 🧾 Licença
Este projeto é de uso pessoal e educativo.  
Sinta-se livre para adaptar e redistribuir com créditos ao autor original.
