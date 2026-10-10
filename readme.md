# Atelier Aline Gouveia

Catálogo online de um ateliê de peças artesanais, com carrinho de compras, painel administrativo e finalização de pedidos pelo WhatsApp.

O projeto foi pensado para pequenos negócios que querem vender sem a complexidade de uma loja virtual completa: a proprietária gerencia os produtos pelo próprio celular e o cliente conclui o pedido em uma conversa.

🔗 **[Acessar o site](https://SEU-ENDERECO-AQUI)**

## Destaques

- Interface elegante e responsiva, com visual delicado e identidade própria (logo em SVG com agulha e linha)
- Catálogo organizado em grupos, com filtro por categoria:
  - **Mesa:** Centro de mesa, Sousplat/Americanos e Trilhos de mesa
  - **Casa:** Passadeiras, Jogos de banheiro e Tapetes
  - **Moda:** Moda praia e Blusas
- Badges de **Promoção**, **Novo** e **Mais vendido**, com preço anterior riscado nas promoções
- Carrinho com controle de quantidade, subtotal por item e total da compra
- Pedido enviado ao WhatsApp em mensagem organizada e pronta para atendimento
- Botão flutuante de WhatsApp e link para o Instagram do ateliê
- Painel administrativo com login, para cadastrar, editar e excluir produtos e imagens
- Catálogo atualizado em tempo real, sem recarregar a página

## Tecnologias

| Camada | Tecnologia |
|---|---|
| Interface | HTML, CSS e JavaScript (ES Modules) |
| Banco de dados | Firebase Firestore |
| Autenticação | Firebase Authentication |
| Imagens | Cloudinary |

## Como funciona

```
Cliente ──► Site (HTML/CSS/JS) ──► Firestore (produtos, em tempo real)
                │
                └──► WhatsApp (pedido formatado)

Administradora ──► Login (Firebase Auth) ──► Painel ──► Firestore + Cloudinary (imagens)
```

O site é estático e usa serviços em nuvem no lugar de um servidor próprio. A escrita no banco é restrita à administradora por regras de segurança do Firestore.

## Executando localmente

1. Clone o repositório:
   ```bash
   git clone https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
   ```
2. Abra a pasta e inicie um servidor local (por exemplo, a extensão **Live Server** do VS Code).
3. Acesse o endereço indicado no navegador.

Sem credenciais configuradas, o site abre em **modo demonstração**, com produtos de exemplo, e é possível testar o catálogo, o carrinho e o painel.

Para conectar ao seu próprio Firebase e Cloudinary, edite o objeto `CONFIG` no início do arquivo JavaScript.

## Estrutura

```
atelier-aline-gouveia/
├── assets/
│   ├── css/
│   ├── images/
│   └── js/
├── index.html
├── .gitignore
└── README.md
```

## Próximos passos

- Remoção automática das imagens no Cloudinary ao excluir um produto
- Dados do cliente (nome e endereço) incluídos no pedido
- Busca de produtos
- Histórico de pedidos

## Autor

Desenvolvido por **Alan Dias** · [LinkedIn](https://www.linkedin.com/in/alanpedrodiasdesenvolvedor/) · [Portfólio](https://portfolio-alan-dias-liart.vercel.app/)