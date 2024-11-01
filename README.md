# Atividade 7: T3

**Alix D Avellar Pretto Sanches**  
RA: 10395951  

**Murilo Senaga**  
RA: 10395789  

---

## API OpenGL:

OpenGL é uma API gráfica aberta e multiplataforma utilizada para renderizar gráficos 2D e 3D. Desenvolvida inicialmente pela Silicon Graphics (SGI) nos anos 90, ela se tornou um padrão amplamente adotado por sistemas operacionais, como Windows, macOS e Linux, além de ser suportada em dispositivos móveis e consoles. OpenGL é amplamente usado na indústria devido à sua flexibilidade e capacidade de funcionar em diversos dispositivos, sendo especialmente útil para programadores que precisam de controle direto sobre a renderização gráfica.

A maior parte das implementações do OpenGL tem uma ordem de operações a serem executadas. Uma série de estágios de processos compõem o “pipeline” de renderização do OpenGL. O diagrama a seguir mostra como o OpenGL obtém e processa os dados. 

### Listas de Exposição

Todos os dados, se descrevem uma geometria ou pixels, podem ser conservados em uma lista de exposição para uso corrente ou serem usados mais tarde. (A alternativa além de manter dados em uma lista de exposição é processar os dados imediatamente – também conhecido como modo imediato.) Quando uma lista de exposição é executada, os dados retidos são enviados da lista apenas como se fossem enviados pela aplicação no modo imediato.

A OpenGL documenta a pipeline gráfica como uma sequência de etapas, divididas principalmente entre a fase de processamento de vértices e a fase de rasterização, como mostrado abaixo:

1. **Entrada de Dados**
   - **Descrição:** O pipeline começa com a entrada de vértices, cores e texturas fornecidos pelo programador.
   - **API:** O desenvolvedor define buffers e arrays de vértices (VBOs e VAOs).

2. **Shader de Vértice (Vertex Shader)**
   - **Função:** Cada vértice é transformado, aplicando projeção, translação ou rotação.
   - **API:** Os desenvolvedores escrevem shaders personalizados usando GLSL.

3. **Montagem de Primitivas**
   - **Descrição:** Os vértices são combinados para formar primitivas (pontos, linhas ou triângulos).

4. **Rasterização**
   - **Função:** Converte as primitivas em fragmentos (potenciais pixels na tela).
   - **Detalhe na documentação:** OpenGL explica como cada tipo de primitiva é rasterizado (como triângulos e linhas).

5. **Shader de Fragmento (Fragment Shader)**
   - **Função:** Cada fragmento é processado para definir sua cor final.
   - **API:** O desenvolvedor controla cores, sombras e texturas.

6. **Teste e Descarte (Depth/Stencil Test)**
   - **Descrição:** Fragmentos que não atendem a certos critérios (como profundidade) são descartados.

7. **Mesclagem (Blending)**
   - **Função:** Fragmentos aprovados são mesclados com os já renderizados para gerar efeitos de transparência.

8. **Exibição na Tela**
   - **Descrição:** Os dados finalizados são enviados ao framebuffer para serem exibidos como pixels na tela.

### Documentação da OpenGL sobre a Pipeline

- A OpenGL oferece uma visão modular da pipeline gráfica, explicando cada etapa com detalhes e exemplos.
- Diagramas são frequentemente usados para ilustrar a sequência de processamento.
- Especificações técnicas explicam como cada etapa é controlada por estados e shaders.
- **GLSL Reference Manuals** detalham como escrever shaders compatíveis com cada etapa da pipeline.

---

## Linguagens Suportadas:

- **GLSL (OpenGL Shading Language)**
   - **Shaders suportados:**
     1. **Vertex Shader:** Processa vértices individuais.
     2. **Fragment Shader:** Define a cor dos fragmentos (potenciais pixels).
     3. **Geometry Shader:** Gera novos vértices com base em primitivas (opcional).
     4. **Tessellation Shaders:** Controla a subdivisão de malhas para renderização mais detalhada.

- **SPIR-V** (Standard Portable Intermediate Representation - Vulkan)
- **Cg** (C for Graphics)
- **ARB Assembly Language**

---

## Blender

O Blender é um software de código aberto para modelagem 3D, animação, simulação, renderização e edição de vídeo. Ele é amplamente utilizado na indústria para criar filmes, jogos, e gráficos 3D. O Blender faz uso da API OpenGL para renderizar objetos 3D em tempo real na viewport (janela de visualização) e permitir a manipulação interativa de modelos e animações.

---

### Referências:

- [Wikipedia: OpenGL](https://pt.wikipedia.org/wiki/OpenGL)  
- [Programaê: Glossário - O que é OpenGL e para que serve?](https://programae.org.br/termos/glossario/o-que-e-opengl-e-para-que-serve/)  
- [UFAL: OpenGL](https://ic.ufal.br/professor/thales/OpenGL.pdf)  
- [ChatGPT](https://chatgpt.com)
