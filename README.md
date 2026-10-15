<div align="center">

<img src="src/icons/128x128@2x.png" alt="Arcanum" width="112" />

# Arcanum

**Onde a magia ganha páginas.**

Editor de livros inteligente, com somente o essencial:<br />
binder, editor, notas, pesquisa, variáveis e compilação para os formatos que importam.

![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-0b0b0b?style=flat-square)
![macOS](https://img.shields.io/badge/macOS-0b0b0b?style=flat-square&logo=apple)
![Última versão](https://img.shields.io/github/v/release/danillo-ao/arcanum-releases?style=flat-square&color=0b0b0b&label=vers%C3%A3o)

**[⬇ Baixar a última versão](https://github.com/danillo-ao/arcanum-releases/releases/latest)**

</div>

---

Este repositório guarda **só as builds prontas** do Arcanum. É daqui que o app baixa as atualizações em **Ajuda › Buscar atualizações…**. O código-fonte fica em outro repositório, privado.

## Qual arquivo baixar

Abra a [última versão](https://github.com/danillo-ao/arcanum-releases/releases/latest) e escolha em **Assets**:

| Sistema | Arquivo |
|---|---|
| Windows 10/11 (64 bits) | `Arcanum_X.Y.Z_x64-setup.exe` |
| macOS com Apple Silicon (M1, M2…) | `Arcanum_X.Y.Z_aarch64.dmg` |
| macOS com Intel | `Arcanum_X.Y.Z_x64.dmg` |

Os outros arquivos (`.app.tar.gz` e `latest.json`) são usados pelo atualizador do app. Não é preciso baixá-los.

> Uma versão pode sair primeiro para um sistema e depois para o outro. Se o arquivo do seu sistema ainda não estiver lá, use a versão anterior por enquanto.

## Instalação

### Windows

1. Rode o `Arcanum_X.Y.Z_x64-setup.exe`.
2. Como o app não tem assinatura de código da Microsoft, o SmartScreen pode avisar "O Windows protegeu o computador". Clique em **Mais informações › Executar assim mesmo**.
3. O instalador confere se o **Pandoc** e o **Typst** estão instalados e, se faltarem, instala os dois pelo `winget`. Eles são usados na compilação (PDF, EPUB, DOCX etc.).

### macOS

1. Abra o `.dmg` e arraste o **Arcanum** para a pasta **Aplicativos**.
2. Como o app não é assinado pela Apple, a primeira abertura exige **clique direito no app › Abrir › Abrir**. Se o macOS disser que o app "está danificado", rode no Terminal:

   ```bash
   xattr -cr /Applications/Arcanum.app
   ```

3. Instale o Pandoc e o Typst, usados na compilação:

   ```bash
   brew install pandoc typst
   ```

Isso só é preciso na primeira instalação. As atualizações seguintes abrem normalmente.

## Atualizações

O Arcanum se atualiza sozinho: use **Ajuda › Buscar atualizações…** ou ligue a busca automática em **Configurações › Atualizações**. Quando há versão nova, o app mostra as notas e oferece **Instalar e reiniciar**, **Lembrar depois** ou **Ignorar esta versão**.

- Antes de instalar, o app grava o texto pendente e faz um backup do projeto aberto.
- Cada atualização é conferida com uma chave de assinatura própria do Arcanum. Um arquivo alterado ou de outra origem é recusado.
- No Windows, o instalador roda sozinho com uma barra de progresso e reabre o app. No macOS, o app é substituído no lugar e reinicia.

## Seus dados

O Arcanum é para uso **local e pessoal**: não tem conta, nuvem nem telemetria. Os projetos ficam em pastas comuns no seu disco, e nada sobre você ou seus textos é enviado para lugar nenhum. A busca de atualizações só lê o `latest.json` deste repositório.
