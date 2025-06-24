# Mirror Notes Plugin

Um plugin para Obsidian que renderiza templates dinâmicos dentro do editor usando CodeMirror 6.

## Status Atual

O plugin está funcional com renderização básica de templates. O widget aparece dentro do editor quando uma nota tem `type: project` no frontmatter.

### ✅ Funcionalidades Implementadas
- Detecção de frontmatter `type: project`
- Renderização de templates Markdown
- Widget integrado ao scroll do editor
- Substituição de variáveis do template
- Botão para fechar o widget
- Re-renderização ao mudar frontmatter

### 🚧 Problemas Conhecidos
- Widget está duplicando conteúdo como texto ao invés de renderizar
- Precisa implementar melhor integração com CodeMirror para evitar conflitos
- Falta sistema de settings para configurar templates

## Estrutura do Projeto
mirror-notes/
├── main.ts                       # Plugin principal
├── src/
│   └── editor/
│       ├── mirrorWidget.ts      # Widget que renderiza templates
│       ├── mirrorState.ts       # Gerenciamento de estado
│       └── mirrorViewPlugin.ts  # Plugin do CodeMirror
├── manifest.json                # Metadados do plugin
├── styles.css                   # Estilos
└── templates/
└── test-template.md         # Template de exemplo

## Próximos Passos

1. **Corrigir renderização**: O widget deve usar decorações do CodeMirror ao invés de inserir DOM diretamente
2. **Implementar settings**: Interface para configurar templates por tipo
3. **Integração com meta-bind**: Permitir inputs interativos
4. **Suporte a múltiplos templates**: Sistema de mapeamento tipo → template

## Desenvolvimento

```bash
# Instalar dependências
npm install

# Desenvolvimento com hot reload
npm run dev

# Build para produção
npm run build
Arquivos Relevantes para Continuação
Para continuar o desenvolvimento, são necessários:

main.ts
src/editor/mirrorWidget.ts
src/editor/mirrorState.ts
src/editor/mirrorViewPlugin.ts
manifest.json
package.json


## 3. Comandos Git:

```bash
# Inicializar repositório (se ainda não fez)
git init

# Adicionar arquivos
git add .

# Criar .gitignore
echo "node_modules/
main.js
.hotreload/
.DS_Store" > .gitignore

# Commit inicial
git commit -m "feat: initial implementation of Mirror Notes plugin with CodeMirror integration

- Added CodeMirror-based widget system for rendering templates
- Implemented frontmatter detection for type:project
- Created state management with StateField
- Added basic template rendering with variable substitution
- Known issue: widget content rendering as plain text"