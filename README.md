# 📝 Tech Course Registration Form

Formulário de inscrição para alunos interessados em um workshop de programação, feito apenas com **HTML**.

## 🙋 Sobre o projeto

Este é um **PP (Projeto Próprio)**: eu mesmo montei este formulário para praticar a estrutura de formulários em HTML, usando o que aprendi sobre `form`, `fieldset`, `label`, `input`, `select` e `textarea`.

## 🧱 Estrutura do formulário

O formulário (`<form id="survey-form">`) é dividido em quatro grupos (`<fieldset>`), cada um com um título (`<legend>`), e termina com um botão de envio.

```text
header
├── h1 (título)
└── p (descrição)

form#survey-form
├── fieldset: Personal info
│   ├── Name              (input text)
│   ├── E-mail            (input email)
│   ├── Age               (input number)
│   └── Experience Level  (select)
├── fieldset: Employment Status
│   ├── Student           (input radio)
│   └── Employed          (input radio)
├── fieldset: What do you want to learn?
│   ├── HTML5 & CSS Fundamentals (input checkbox)
│   ├── JavaScript               (input checkbox)
│   ├── Cybersecurity & Network  (input checkbox)
│   └── Back-End                 (input checkbox)
├── fieldset: Comments
│   └── Comments          (textarea)
└── button Submit
```

## 📋 Campos

| Grupo | Campo | Tag / tipo | Obrigatório | Detalhes |
| --- | --- | --- | --- | --- |
| Personal info | Name | `input type="text"` | Sim | `placeholder="Your name"` |
| Personal info | E-mail | `input type="email"` | Sim | O navegador valida o formato do e-mail |
| Personal info | Age | `input type="number"` | Sim | `min="5"` e `max="100"` |
| Personal info | Experience Level | `select` | Sim | Três opções, mais uma opção inicial desativada ("Select an option") |
| Employment Status | Student / Employed | `input type="radio"` | Não | Mesmo `name="employment"`, então só uma opção pode ser marcada |
| What do you want to learn? | Tópicos | `input type="checkbox"` | Não | Mesmo `name="topics"`, então é possível marcar vários |
| Comments | Comments | `textarea` | Não | `rows="4"` e `cols="30"` |

### Opções de "Experience Level"

| Valor (`value`) | Texto exibido |
| --- | --- |
| `advanced` | I build cool stuff already |
| `basic` | I know the basics |
| `zero` | Honestly? No idea! |

## 🔑 O que cada parte faz

- **`<label for="...">` + `id`:** cada campo tem um `label` ligado a ele pelo `for`, que é igual ao `id` do campo. Clicar no texto foca ou marca o campo.
- **`name`:** é o nome com que o dado seria enviado. Nos `radio`, o mesmo `name` forma um grupo de escolha única. Nos `checkbox`, o mesmo `name` agrupa os tópicos.
- **`required`:** impede o envio enquanto o campo estiver vazio.
- **`placeholder`:** mostra um exemplo dentro do campo antes de digitar.
- **`min` / `max`:** limitam a idade aceita (de 5 a 100).
- **`disabled selected` na primeira `<option>`:** a opção "Select an option" aparece como texto inicial, mas não pode ser escolhida de novo.
- **`<button type="submit">`:** envia o formulário e aciona a validação do navegador.

## ♿ Acessibilidade

- Todos os campos têm `label` associado.
- Os grupos de `radio` e `checkbox` usam `fieldset` e `legend`.
- O campo de e-mail usa `type="email"`, o que também ajuda o teclado do celular.

## ▶️ Como usar

1. Baixe ou clone este repositório.
2. Abra o arquivo `index.html` no navegador.
3. Preencha os campos e clique em **Submit** para ver a validação em ação.

> ℹ️ O formulário ainda não tem `action` nem `method`, então não envia os dados para nenhum servidor. Ele serve como estudo da estrutura e da validação nativa do HTML.

## 🛠️ Tecnologias

- HTML5

## 👤 Autor

**Caio Rafael-dev**, estudante de Full Stack e InfoSec.