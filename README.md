# Fellipe Menezes · Studio de Musculação

Página de links do **Fellipe Menezes · Studio de Musculação**, em Prata, MG. Foi feita para abrir ao aproximar um cartão NFC do celular e tirar as dúvidas mais comuns: falar no WhatsApp, ver o Instagram, avaliar no Google e saber como chegar.

## O que tem na página

- Botão de **WhatsApp** com mensagem pronta
- Link para o **Instagram**
- **Avaliação no Google**, abrindo direto a janela de estrelas
- **Como chegar**, abrindo a rota no Google Maps
- **Copiar endereço**, para colar em qualquer app de mapas
- Selo **Aberto agora / Fechado** (opcional, aparece quando os horários são preenchidos)
- Tema **claro e escuro**, que segue o celular e lembra a escolha da pessoa
- Animações leves, que respeitam quem usa "reduzir movimento"
- Arquivo único, sem frameworks, rápido de carregar no 4G

## Estrutura

```
.
├── index.html   # a página inteira (HTML, CSS, JS e logos embutidos)
└── README.md
```

## Como editar

Todas as informações ficam no bloco `CONFIG`, no final do `index.html`:

| Campo | O que faz |
|---|---|
| `whatsappNumero` | Número com país e DDD, só dígitos (ex.: `5534998767030`) |
| `whatsappMensagem` | Texto que já vem escrito no WhatsApp |
| `instagram` | Link do perfil |
| `googlePlaceId` | Place ID do Google, usado no botão de avaliação |
| `googleFallback` | Link reserva caso o Place ID esteja vazio |
| `endereco` | Endereço usado na rota e no botão de copiar |
| `horarios` | Horário de funcionamento (veja abaixo). `null` esconde o selo |

### Horário de funcionamento

Os dias vão de `0` (domingo) a `6` (sábado), no formato `"HH:MM"`:

```js
horarios: {
  1: ["06:00", "21:00"],
  2: ["06:00", "21:00"],
  3: ["06:00", "21:00"],
  4: ["06:00", "21:00"],
  5: ["06:00", "21:00"],
  6: ["08:00", "12:00"]
}
```

Dias que não aparecem na lista contam como fechados.

## Publicar no GitHub Pages

1. Envie o `index.html` para a raiz do repositório.
2. Vá em **Settings → Pages**.
3. Em **Source**, escolha **Deploy from a branch**, branch **main**, pasta **/(root)**, e clique em **Save**.
4. Aguarde de 1 a 3 minutos. O link aparece na mesma tela.

Para atualizar o site, edite o `index.html` direto no GitHub (ícone de lápis) e clique em **Commit changes**. O site é atualizado em cerca de 1 minuto.

## Domínio próprio

Para gravar no cartão NFC, o ideal é usar um domínio próprio, como `fellipemenezes.com.br`. Assim o endereço do cartão não muda mesmo que o site troque de hospedagem.

Em **Settings → Pages → Custom domain**, informe o domínio e siga as instruções de DNS. O HTTPS é gratuito.

Depois de publicar, no `<head>` do `index.html`, descomente as linhas `og:url`, `og:image` e `canonical` e troque `SEUDOMINIO` pelo seu endereço. Assim o link mostra uma prévia bonita ao ser compartilhado.

## Dicas para o cartão NFC

- Grave na tag o endereço definitivo, com `https://`.
- Teste em um Android e em um iPhone antes de produzir os cartões.
- Inclua um **QR code** no cartão para quem estiver com o NFC desligado.

## Contato

- WhatsApp: (34) 99876-7030
- Instagram: [@fellipemenezespersonal](https://www.instagram.com/fellipemenezespersonal)
- Endereço: R. Jesus Vilela Oliveira, 94 · Edna, Prata, MG · 38140-000
