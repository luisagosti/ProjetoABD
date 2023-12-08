# ProjetoABD
## Diagrama UML

### Classes:

#### Passageiro:

**Atributos:**
- ID_Passageiro: int (PK)
- Nome: string
- Tipo_Bagagem: string

**Métodos:** (dependendo dos requisitos específicos)

#### Voo:

**Atributos:**
- ID_Voo: int (PK)
- N_Assentos_Disponiveis: int
- Tipo_Aviao: string

**Métodos:** (dependendo dos requisitos específicos)

#### Assento:

**Atributos:**
- ID_Assento: int (PK)
- Numero_Assento: string
- Fila: int
- Coluna: string
- Tipo_Assento: string (Janela, Corredor, etc.)

**Métodos:** (dependendo dos requisitos específicos)

#### Reserva:

**Atributos:**
- ID_Reserva: int (PK)
- ID_Passageiro: int (FK)
- ID_Voo: int (FK)
- ID_Assento: int (FK)
- Preco_Total: float

**Métodos:** (dependendo dos requisitos específicos)

### Relacionamentos:

#### Passageiro (1:N) Reserva (N:1) Voo:

- Associação bidirecional entre Passageiro e Reserva.
- Associação bidirecional entre Reserva e Voo.

#### Voo (1:N) Assento:

- Associação bidirecional entre Voo e Assento.

#### Reserva (N:1) Assento:

- Associação bidirecional entre Reserva e Assento.

### Tipos de Chave:

**Chaves Primárias (PK):**
- ID_Passageiro em Passageiro
- ID_Voo em Voo
- ID_Assento em Assento
- ID_Reserva em Reserva

**Chaves Estrangeiras (FK):**
- ID_Passageiro em Reserva
- ID_Voo em Reserva
- ID_Assento em Reserva

### Tipos de Dados:

- Inteiro (int): Utilizado para representar IDs, quantidades, etc.
- String: Utilizado para representar nomes, tipos de bagagem, etc.
- Float: Utilizado para representar valores monetários.

