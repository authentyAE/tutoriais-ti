# Modelo de configuração dos computadores Novos (Escritório MDC Projetos)

Este arquivo contem os passos para a configuração inicial do Windows nos computadores novos da *MDC Projetos* e *Authenty*.


### Configuração Básica

- [ ] **1 - Instalação do Windows** (se já não tiver vindo de fábrica);
  - [ ] Criar usuário `Admin` com a respectiva senha padrão;
  - [ ] Criar usuário `Producao1`, com a respectiva senha padrão;
- [ ] **2 - Configuração de Rede**
  - [ ] Nomear o PC como `MICRO-XX`, de acordo com a numeração atual;
  - [ ] Definir o IP fixo da máquina no Unify, de modo que siga o número `XX` da máquina contando a partir do 50;
  - [ ] Configurar como rede Doméstica;
  - [ ] Habilitar acesso SSH;
  - [ ] Habilitar o acesso remoto por RDP para todos os usuários;
  - [ ] Adicionar credenciais de rede, em ambos usuários, para `\\mdcserver`;
  - [ ] Mapear uma unidade de rede `M:\`  para `\\mdcserver\MDC`;
- [ ] **3 - Instalação dos Softwares Básicos** (Instaladores disponíveis no `\\mdcserver`)
  - [ ] * **Softwares Garratech** (agente e antivirus)
  - [ ] UltraVNC (Viewer e Server)
    - [ ] definir senha de somente visualização como `a` e de controle como `aa`
  - [ ] 7zip
  - [ ] kLite Codec pack - Mega
  - [ ] OnlyOffice Desktop Editors
  - [ ] PowerToys
  - [ ] VLC Media Player
  - [ ] Google Chrome
  - [ ] Authenty Passwords - [instalação conforme tutorial](./Instalando%20o%20Authenty%20Passwords%20(programa%20de%20senhas).md)
  - [ ] Python
  - [ ] Java Runtime
  - [ ] Foxit PDF Reader
    - NÃO instalar teste de 30 dias
    - NÃO instalar extensão de navegador nem nada adicional
  - [ ] Space Sniffer (Colar executável direto em `C:\Users\Public\Desktop`)
- [ ] **4 - Instalação do Script de limpeza** (vide item abaixo)
- [ ] **5 - Instalação dos Softwares Específicos** (vide item abaixo)


---


### Script de limpeza

No Startup do windows, colocamos um script de limpeza do PC, que elimina pastas conhecidas do SCIA e força o usuário a limpar algumas pastas.

Siga [este tutorial para instalação do script de startup](https://github.com/williampilger/utilidades_gerais/tree/master/authenty_diversos/startup_script); 


---


### Instalação de Softwares específicos (Engenharia)

Todos os instaladores estão disponíveis em `\\mdcserver\programas_ferramentas\windows\programas_instaladores\1. Softwares Engenharia`.

- **Scia Engineer** (tutorial de instalação junto com o instalador no `\\mdcserver`)
  - [ ] v 26
  - [ ] v 22.1.1025.64
- **Allplan** (tutorial de instalação junto com o instalador no `\\mdcserver`)
  - [ ] v 26-0-1
  - [ ] v 21-1-21
  - `⚠️ ATENÇÃO! Não seguir as orientações da instalação podem causar sobrescrita de informações no servidor!!!`
- [ ] **SketchUp 2019 PRO** (Não ativar o produto. Só é ativado quando usado)
- [ ] **ZWCad** (Orientações sobre licença flutuante com o instalador em `\\mdcserver`)
- [ ] **BIMcollab ZOOM - Free**
- [ ] **VisualVentos**
- **Portable Softwares** (Executáveis que devem ser copiados para `C:\Users\Public\Desktop`)
  - [ ] Ftool
  - [ ] PCalc 1.4
  - [ ] SECC-1.0.0


---


## Sobre

<div align="center">
  <img src="https://github.com/williampilger.png" alt="William Pilger" style="border-radius: 50%; margin-bottom: 10px; width: 100px">
  
  **Criado por: [William Pilger](https://github.com/williampilger)**  
  *COO | Authenty - Softwares para Engenharia*
  
  🌐 [authenty.com.br](http://authenty.com.br/) | [@authentyAE](https://github.com/authentyAE)  
  
  **Escrito em:** *17 de outubro de 2025, 11:08*  
</div>

---

<div align="center">
  <sub>
    💡 <em>Este tutorial faz parte da coleção de documentações técnicas da <strong>MDC Projetos<strong>.</em><br>
    📚 Encontre mais tutoriais em: <a href="https://github.com/authentyAE/tutoriais-ti">github.com/authentyAE/tutoriais-ti</a>
  </sub>
</div>