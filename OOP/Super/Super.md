## 🔹 Super() – O que é?

`super()` é um conceito utilizado dentro do contexto de **Programação Orientada a Objetos (POO)**. Ele permite que subclasses acessem métodos ou atributos da **superclasse (classe mãe)**, evitando repetição de código e facilitando a extensão de funcionalidades.

---

## 🔹 Exemplo prático

Imagine um universo de personagens de fantasia com **arqueiros** e **bruxos**. Ambos possuem características semelhantes, como:

- Nome
- Descrição
- Altura
- Local de origem
- Poder de combate
- Vigor

Porém, cada um também tem características específicas:

- O **bruxo** possui magias.
- O **arqueiro** possui quantidade de flechas.

Para organizar essas similaridades e diferenças, criamos uma **classe mãe** chamada `Personagem`, que engloba os atributos comuns (ex: nome e pontos de combate). Tanto o arqueiro quanto o bruxo serão subclasses de `Personagem`, herdando essas propriedades básicas.

Assim:

- **Classe mãe (superclasse)**: `Personagem`
- **Classes filhas (subclasses)**: `Arqueiro` e `Bruxo`

- `The super() function is used to give access to methods and properties of a parent or sibling class.`
- `The super() function returns an object that represents the parent class.`

