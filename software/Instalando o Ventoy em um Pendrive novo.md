# Tutorial: Como Instalar o Ventoy em um Pendrive

O Ventoy é uma ferramenta que permite criar um pendrive bootável capaz de carregar múltiplas imagens ISO sem precisar reformatar o pendrive a cada nova ISO adicionada.

> **💡 Dica:** Provavelmente o departamento de TI já possui um pendrive com Ventoy instalado. Consulte antes de criar um novo!

---

## 📋 O que você vai precisar

### Hardware
- **Pendrive** (mínimo 8GB, recomendado 16GB ou mais)
- **PC com Windows/Linux**

### Software
- **Ventoy** (download gratuito do site oficial)


---


## 🔧 Passo a Passo

### Passo 1: Download do Ventoy
1. **Acesse** o site oficial: [https://www.ventoy.net](https://www.ventoy.net)
2. **Baixe a versão** para seu sistema operacional:
   - **Windows**: `ventoy-x.x.xx-windows.zip`
   - **Linux**: `ventoy-x.x.xx-linux.tar.gz`
3. **Extraia o arquivo** em uma pasta de sua escolha


### Passo 2: Preparação do Pendrive
1. **Conecte o pendrive** no PC
2. **Faça backup** de dados importantes do pendrive (serão apagados)
3. **Anote a letra/dispositivo** do pendrive


### Passo 3.1: Instalação no Windows

#### Interface Gráfica (Recomendado)
1. **Execute** `Ventoy2Disk.exe` como administrador
2. **Selecione o pendrive** na lista suspensa
3. **Clique em "Install"**
4. **Confirme** a instalação (dados serão apagados)
5. **Aguarde** a conclusão (1-3 minutos)

#### Linha de Comando
```cmd
# Abra CMD como administrador
cd caminho\para\ventoy
Ventoy2Disk.exe /I /GT /L:VENTOY X:
# Substitua X: pela letra do seu pendrive
```


### Passo 3.2: Instalação no Linux

1. **Abra o terminal**
2. **Navegue** até a pasta do Ventoy:
   ```bash
   cd /caminho/para/ventoy
   ```
3. **Execute** o instalador:
   ```bash
   sudo ./VentoyGUI.x86_64
   ```
4. **Selecione o dispositivo** (ex: /dev/sdb)
5. **Clique em "Install"**
6. **Confirme** a instalação


### Passo 4: Adicionar ISOs ao Ventoy

1. **Abra** o pendrive no explorador de arquivos
2. **Copie** os arquivos ISO diretamente para a raiz do pendrive
3. **Organize** em pastas se desejar (opcional):
   ```
   VENTOY (E:)
   ├── Linux/
   │   ├── ubuntu-22.04.iso
   │   └── manjaro-kde.iso
   ├── Windows/
   │   └── Win11_22H2.iso
   └── Utilities/
       ├── clonezilla-live.iso
       └── gparted-live.iso
   ```


## 📁 ISOs Recomendadas para TI

### Sistemas Operacionais
- **Ubuntu 22.04 LTS** - Linux amigável
- **Windows 10/11** - Para instalações
- **Manjaro** - Linux intermediário

### Ferramentas de Diagnóstico
- **Clonezilla Live** - Clonagem de discos
- **GParted Live** - Gerenciamento de partições
- **MemTest86** - Teste de memória RAM
- **Ultimate Boot CD** - Ferramentas diversas



## 🚀 Como Usar o Ventoy

### Inicialização
1. **Conecte** o pendrive no PC
2. **Reinicie** e acesse o menu de boot (F12, F11, F8, ESC)
3. **Selecione** o pendrive Ventoy
4. **Escolha** a ISO desejada no menu do Ventoy
5. **Configure** opções de boot se necessário

### Menu do Ventoy
- **Modo Normal**: Boot padrão da ISO
- **Modo GRUB2**: Para ISOs que requerem GRUB2
- **Modo WIMBOOT**: Para ISOs do Windows
- **Modo RAWBOOT**: Boot direto sem Ventoy



## ⚙️ Configurações Avançadas

### Personalizar Menu
1. **Crie** a pasta `ventoy` na raiz do pendrive
2. **Crie** o arquivo `ventoy.json`:
```json
{
    "theme": {
        "display_mode": "GUI",
        "gfxmode": "1024x768",
        "timeout": 30
    },
    "menu_alias": [
        {
            "image": "/Linux/ubuntu-22.04.iso",
            "alias": "Ubuntu 22.04 LTS Desktop"
        }
    ]
}
```


### Partição de Dados
- **Por padrão**, Ventoy cria duas partições:
  - **Partição 1**: Dados (para ISOs e arquivos)
  - **Partição 2**: Sistema Ventoy (não mexer)
- **Use apenas a primeira partição** para seus arquivos

## 🛠️ Solução de Problemas

### Pendrive não é reconhecido
- **Teste** em outra porta USB
- **Verifique** se é USB 2.0/3.0 compatível
- **Execute** como administrador

### ISO não inicia
- **Verifique** se a ISO não está corrompida
- **Tente** modo GRUB2 ou WIMBOOT
- **Baixe** ISO de fonte confiável

### Boot não funciona
- **Desabilite** Secure Boot na BIOS
- **Configure** BIOS para Legacy/UEFI conforme necessário
- **Verifique** ordem de boot

### Atualização do Ventoy
1. **Execute** novamente o instalador
2. **Escolha** "Update" em vez de "Install"
3. **ISOs e dados** serão preservados

## ⚠️ Importantes Considerações

- **Faça backup** do que tiver no pendrive, por que ele será apagado!
- **Use** pendrives de qualidade para melhor desempenho
- **Mantenha** o Ventoy atualizado
- **Teste** as ISOs após adicionar

---

## 📞 Precisa de Ajuda?

Se encontrou problemas durante a instalação ou tem dúvidas sobre ISOs específicas, entre em contato com a equipe de TI.

**Tempo estimado**: 15-30 minutos  
**Dificuldade**: Básica  
**Risco**: Baixo

---

## 🔗 Links Úteis

- **Site oficial**: https://www.ventoy.net
- **Documentação**: https://www.ventoy.net/en/doc_start.html
- **GitHub**: https://github.com/ventoy/Ventoy
