# Magic Picture Pro

**Editor e conversor de imagens offline para desktop**  
Versão: **1.0 (inicial)** · Idioma: **Português (Brasil)** · Arquivo principal: `Magic_Picture_Pro.html`

## Apresentação

O **Magic Picture Pro** é um aplicativo de edição e conversão de imagens desenvolvido em **HTML, CSS e JavaScript**, para execução local no navegador, sem depender de servidor ou serviços online para as funções implementadas.

Sua interface é inspirada na organização visual do **Fluxo Lab 3.0**, com prancha central, acesso lateral às ferramentas, painel de propriedades e exportação, controles flutuantes de zoom e áreas recolhíveis.

## Ferramentas

| Módulo | Funcionalidade na versão 1.0 |
| --- | --- |
| **Background Remover** | Remove áreas por seleção de cor, com ajuste de tolerância; **não utiliza IA**. |
| **Background Blur** | Aplica desfoque em regiões identificadas por máscara de cor. |
| **Image Upscaler** | Amplia imagens em **2× ou 4×** usando interpolação; **não é super-resolução por IA**. |
| **HEIC Converter** | Tenta abrir arquivos `.heic` / `.heif` por meio da decodificação oferecida pelo navegador; compatibilidade variável. |
| **WEBP Converter** | Abre imagens WEBP compatíveis e exporta em outros formatos. |
| **Borracha manual** | Apaga regiões da imagem diretamente na prancha. |

O aplicativo também conta com **desfazer/refazer**, abertura de imagens e zoom na área de trabalho.

## Formatos de entrada e saída

### Entrada

Utilize **Abrir imagem** ou a área de trabalho. O campo de importação aceita tipos `image/*` e também indica extensões **HEIC, HEIF, BMP, WEBP e SVG**. A leitura efetiva de cada formato depende do suporte de decodificação do navegador; o HEIC/HEIF, em particular, pode não abrir em alguns ambientes.

### Saída — painel único de exportação

Todas as ferramentas compartilham o mesmo painel de exportação. As opções disponíveis são:

| Extensão | Observação |
| --- | --- |
| `.png` | Raster, com suporte a transparência. |
| `.jpg` / `.jpeg` | Raster, sem transparência. |
| `.webp` | Raster; suporte conforme o navegador. |
| `.bmp` | Raster. |
| `.svg` | **Contêiner SVG com imagem raster incorporada**; não transforma pixels em vetores editáveis. |
| `.ico` | Arquivo de ícone, voltado a dimensões pequenas. |

O painel permite ajustar **largura, altura, manutenção da proporção e qualidade**, conforme o formato. O fato de uma extensão estar disponível **não significa que o resultado será vetorial ou que a qualidade aumentará automaticamente**.

> **Nota:** `.ico` é a extensão utilizada para ícones do Windows. `.web` não é um formato de imagem padrão; para imagens na web, utilize `.webp`, `.png`, `.jpg` ou `.svg`, conforme a finalidade.

## Como executar no computador

1. Salve o arquivo `Magic_Picture_Pro.html` em uma pasta local.
2. Abra o arquivo em um navegador moderno, como Chrome ou Edge.
3. Clique em **Abrir imagem** e selecione uma fotografia ou imagem compatível.
4. Escolha a ferramenta na lateral e ajuste os respectivos controles.
5. No painel de exportação, escolha o formato e as dimensões desejadas.
6. Clique em **Exportar imagem** para salvar o resultado.

**Não é necessário instalar pacotes ou configurar APIs** para usar as funcionalidades presentes nesta versão. O arquivo pode ser mantido em um repositório GitHub como página estática; no GitHub Pages, seu acesso inicial depende da internet, ao contrário da abertura local.

## Recomendações de uso

- Prefira **PNG** ao remover áreas e preservar transparência.
- Prefira **JPG** para fotografias quando precisar de arquivos menores e não necessitar de transparência.
- Utilize **WEBP** para publicação na web, quando o ambiente de destino for compatível.
- Utilize **SVG** apenas quando for útil encapsular a imagem em um arquivo SVG; a versão atual **não vetoriza**.
- Utilize **ICO** para ícones e favicons.
- Trabalhe com uma cópia da imagem original e confira o resultado exportado.

## Limitações conhecidas

- A seleção para remoção e desfoque do fundo **é baseada em cor**, podendo afetar elementos com tonalidades semelhantes.
- O ampliador **não recupera detalhes** que não existam na imagem original.
- **HEIC/HEIF** depende de suporte do navegador e do sistema; não há decodificador dedicado empacotado.
- Não há, nesta versão, gerador de imagens por IA nem preenchimento generativo de áreas apagadas.
- A exportação em SVG **não produz vetorização real**.
- O desempenho e o tamanho máximo de imagem dependem da memória e dos limites de Canvas do navegador.
- Esta é uma versão inicial e requer testes de compatibilidade conforme o navegador e os arquivos utilizados.

## Tecnologias

- HTML5
- CSS3
- JavaScript
- Canvas API e recursos nativos de arquivos do navegador

**Execução:** processamento local das funcionalidades existentes. **Sem conta, chave de API ou conexão obrigatória** quando o arquivo é aberto no computador.

## Estrutura do projeto

```text
Magic-Picture-Pro/
├── Magic_Picture_Pro.html   # Aplicativo principal
└── README.md                # Documentação
```

Se o aplicativo for publicado no **GitHub Pages** como site principal do repositório, renomeie uma cópia do arquivo HTML para `index.html`.

## Evoluções possíveis

- Segmentação de pessoas e objetos com modelo de IA offline.
- Remoção de objetos por preenchimento inteligente.
- Ampliação por super-resolução com modelo local.
- Decodificador HEIC/HEIF incluído no próprio pacote.
- Exportação em lote e vetorização real quando tecnicamente aplicável.

Essas funcionalidades **não fazem parte da versão 1.0**.

---

**Magic Picture Pro** — editor de imagens multiuso, com fluxo local de edição e exportação.
