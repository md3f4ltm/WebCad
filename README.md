# WebCad - Visualizador DXF 2D

Visualizador DXF 2D simples e eficiente construído com Three.js e @dxfjs/parser.

## 🚀 Características

- ✅ Visualização 2D de arquivos DXF
- ✅ Suporte para LINE, LWPOLYLINE, POLYLINE, ARC, CIRCLE, POINT e TEXT
- ✅ Renderização de cores (TrueColor e ACI)
- ✅ Pan e zoom com controles intuitivos
- ✅ **Ferramenta de medição ponto-a-ponto**
- ✅ Interface otimizada para desktop, tablet e telemóvel

## 📏 Ferramenta de Medição

### Como usar:

1. **Carregar um arquivo DXF**
   - Clique em "Escolher ficheiro" ou arraste um arquivo DXF para a janela

2. **Ativar modo de medição**
   - Clique no botão **"📏 Medir"** na barra superior
   - O botão ficará azul quando o modo estiver ativo
   - Aparecerá uma barra de ferramentas na parte inferior

3. **Medir distância entre dois pontos**
   - **Primeiro clique:** selecione o primeiro ponto
   - **Segundo clique:** selecione o segundo ponto
   - A distância será calculada e exibida automaticamente
   - Uma linha verde conectará os dois pontos

4. **Fazer nova medição**
   - Clique em **"Cancelar / Nova Medição"** na barra inferior
   - Ou clique novamente no botão "📏 Medir" para desativar

### Características da ferramenta:

- ✨ **Feedback visual em tempo real**: linha de pré-visualização ao mover o cursor após o primeiro ponto
- 🎯 **Precisão**: marcadores verdes nos pontos medidos
- 📱 **Mobile-friendly**: funciona perfeitamente em tablets e telemóveis touchscreen
- 🔢 **Resultado claro**: distância exibida com 3 casas decimais
- 🔄 **Múltiplas medições**: pode fazer quantas medições quiser

### Atalhos:

- **Pan:** Arrastar com o rato/dedo
- **Zoom:** Roda do rato ou pinch no touchscreen
- **Enquadrar:** Botão "Enquadrar" para ajustar visualização

## 🛠️ Tecnologias

- [Three.js](https://threejs.org/) - Renderização 3D/2D
- [@dxfjs/parser](https://github.com/dotbim/dxf) - Parse de arquivos DXF
- OrbitControls - Controles de câmera

## 📱 Compatibilidade

- ✅ Desktop (Chrome, Firefox, Safari, Edge)
- ✅ Tablets (iPad, Android)
- ✅ Telemóveis (iOS, Android)

## 🚀 Como usar localmente

1. Clone o repositório:
```bash
git clone git@github.com:md3f4ltm/WebCad.git
cd WebCad
```

2. Abra o arquivo `index.html` no seu navegador
   - Ou use um servidor HTTP local:
```bash
python -m http.server 8000
# Depois acesse http://localhost:8000
```

## 📂 Estrutura

```
WebCad/
├── index.html          # Aplicação principal
├── examples_dxf/       # Arquivos DXF de exemplo
│   ├── bridge.dxf
│   └── cube.dxf
└── README.md          # Este arquivo
```

## 🐛 Debug

O visualizador expõe variáveis globais para debug:

```javascript
// No console do navegador:
console.log(window.__lastParsedDXF);     // Dados parseados do DXF
console.log(window.__lastDXFText);       // Texto raw do arquivo DXF
console.log(state.group.children);        // Geometrias renderizadas
```

## 📝 Notas

- As coordenadas são exibidas no sistema de coordenadas do DXF
- A ferramenta de medição calcula distâncias euclidianas no plano 2D
- Cores são mapeadas usando TrueColor (24-bit) ou AutoCAD Color Index (ACI)

## 🤝 Contribuir

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests.

## 📄 Licença

Este projeto usa bibliotecas de código aberto:
- Three.js (MIT License)
- @dxfjs/parser (MIT License)

---

Desenvolvido com ❤️ para visualização de desenhos técnicos