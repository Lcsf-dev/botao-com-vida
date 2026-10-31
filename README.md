# ✨ Botão com Vida!

Experimento de interface com HTML, CSS e JavaScript: um botão que pulsa ao passar o mouse e completa uma volta ao ser acionado.

## 🎯 Objetivo

Explorar animações CSS e eventos de interação em uma página estática, sem bibliotecas ou dependências externas.

## 🖱️ Funcionalidades

- Pulsação ao passar o mouse sobre a área do botão, em dispositivos com suporte a hover.
- Rotação de 360° ao clicar ou acionar o botão pelo teclado.
- Bloqueio de novas rotações enquanto uma volta está em andamento.
- Adaptações de layout para telas estreitas e de pouca altura.
- Respeito à preferência do sistema por movimento reduzido.

## 🛠️ Tecnologias

| Tecnologia | Uso |
| --- | --- |
| HTML5 | Estrutura da página e botão nativo |
| CSS3 | Aparência, animações e adaptações de layout |
| JavaScript | Eventos e controle da rotação |
| SVG | Ícone incorporado ao botão |

## 📁 Estrutura

```text
desafio-front-end-botao-com-vida/
├── index.html   # Estrutura da página e JavaScript
├── style.css    # Estilos e animações
└── README.md    # Documentação
```

## 🚀 Como executar

1. Baixe ou clone o repositório.
2. Abra o arquivo `index.html` no navegador.
3. Interaja com o botão usando mouse ou teclado.

Não é necessário instalar pacotes, configurar um servidor ou executar uma compilação. Use um navegador atualizado para aproveitar os recursos de CSS utilizados.

## ⌨️ Como interagir

| Ação | Resultado |
| --- | --- |
| Passar o mouse sobre a área do botão | Ativa a pulsação |
| Clicar no botão | Executa uma volta completa |
| Pressionar Enter | Aciona o botão, inclusive sem foco |
| Pressionar Espaço com o botão em foco | Aciona o botão |
| Pressionar Tab | Permite navegar até o botão |

Com a preferência de movimento reduzido ativada, as animações e transições são desativadas.

## 🧠 Como funciona

A pulsação e a rotação ficam em elementos separados (`.pulso` e `.rotacao`), permitindo combinar os dois movimentos.

No CSS, a propriedade personalizada `--escala-pulso` controla a intensidade da pulsação e permite suavizar a saída do mouse. A animação `girar` executa uma volta completa.

O JavaScript adiciona a classe `girando` para iniciar a rotação. Ao terminar ou cancelar a animação, essa classe é removida, permitindo uma nova interação. Durante uma rotação, novos cliques não reiniciam o movimento.

Uma alteração na preferência de movimento reduzido também remove a classe de rotação.

## ♿ Recursos de acessibilidade

- Botão HTML nativo com suporte a teclado.
- Indicador visual de foco com `:focus-visible`.
- Instruções associadas ao botão com `aria-describedby`.
- Identificação da seção com `aria-labelledby`.
- Elementos decorativos ocultos de tecnologias assistivas com `aria-hidden`.
- Animações e transições desativadas com `prefers-reduced-motion`.

## 🎨 Personalização

As cores e durações principais ficam no bloco `:root` de `style.css`:

| Variável | Finalidade |
| --- | --- |
| `--cor-fundo` | Cor de fundo |
| `--cor-botao` | Cor principal do botão |
| `--cor-botao-clara` | Cor clara do gradiente do botão |
| `--cor-texto` | Cor principal dos textos |
| `--cor-secundaria` | Cor dos textos secundários |
| `--duracao-pulso` | Duração de cada ciclo de pulsação |
| `--duracao-rotacao` | Duração de uma volta |

## ✅ Roteiro de conferência manual

- [ ] Verificar a pulsação ao passar o mouse e sua saída suave.
- [ ] Verificar uma volta completa por acionamento.
- [ ] Clicar repetidamente durante a rotação e conferir que ela não reinicia.
- [ ] Testar Tab, Enter e Espaço.
- [ ] Conferir a interface em telas estreitas e de pouca altura.
- [ ] Ativar a preferência de movimento reduzido e conferir que não há animações.
- [ ] Alterar essa preferência durante uma volta e conferir que o botão continua utilizável.

O roteiro serve para validação manual; o projeto não possui suíte de testes automatizados.
