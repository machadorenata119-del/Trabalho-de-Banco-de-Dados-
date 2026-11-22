🍽️ NutriWaste – Sistema de Gestão e Monitoramento do Desperdício de Alimentos

📌 Sobre o Projeto

O NutriWaste é um projeto desenvolvido com o objetivo de auxiliar na gestão e no monitoramento do desperdício de alimentos em refeitórios corporativos.

O sistema permite acompanhar o planejamento dos cardápios, o preparo das refeições, o atendimento ao público e o registro das sobras alimentares.

A proposta é utilizar dados para apoiar decisões, reduzir custos operacionais e diminuir os impactos ambientais causados pelo desperdício de alimentos.

🎯 Objetivos

- Monitorar o desperdício de alimentos.
- Organizar o planejamento dos cardápios.
- Registrar a quantidade de refeições preparadas.
- Controlar as sobras da cozinha e dos pratos.
- Calcular indicadores de desperdício por pessoa.
- Apoiar a redução de custos e impactos ambientais.

🗂️ Estrutura do Banco de Dados

O banco de dados foi organizado em cinco entidades principais:

Tabela| Descrição
CATEGORIA_PRATO| Armazena as categorias dos alimentos.
PRATO| Registra os pratos e seus custos estimados.
CARDAPIO| Armazena os cardápios planejados.
ITEM_CARDAPIO| Relaciona os pratos aos cardápios e suas quantidades.
REGISTRO_DESPERDICIO| Registra as medições de desperdício das refeições.

🔗 Relacionamentos

O modelo utiliza chaves primárias (PK) e chaves estrangeiras (FK) para organizar os relacionamentos entre as tabelas.

- Uma categoria pode possuir vários pratos.
- Um cardápio pode conter vários pratos.
- A tabela ITEM_CARDAPIO relaciona cardápios e pratos.
- Um cardápio pode possuir um registro de desperdício.

📊 Indicador de Desperdício

O projeto utiliza o indicador de desperdício médio por pessoa.

Fórmula:

(peso_sobra_cozinha_kg + peso_sobra_prato_kg)
 / qtd_pessoas_atendidas

Esse cálculo permite identificar a quantidade média de alimentos desperdiçados por pessoa atendida.

⚙️ Regras de Negócio

- Data, turno e público estimado são obrigatórios.
- Os pesos registrados devem ser positivos.
- A quantidade de pessoas atendidas deve ser maior que zero.
- As sobras totais não podem ultrapassar o peso preparado.
- Cada cardápio pode possuir apenas um registro de desperdício.

🧪 Dados para Validação

O povoamento inicial prevê:

- 4 categorias de alimentos.
- 5 pratos cadastrados.
- 3 cardápios.
- Registros de medição de desperdício.

📐 Normalização

O banco de dados foi estruturado seguindo as três formas normais:

- 1FN: atributos atômicos e ausência de grupos repetitivos.
- 2FN: dependência integral da chave primária composta na tabela ITEM_CARDAPIO.
- 3FN: ausência de dependências transitivas e utilização de métricas calculadas.

👥 Atores do Sistema

- Nutricionista / Gestor da Cozinha: cadastra cardápios e analisa indicadores.
- Auxiliar de Cozinha / Operador: registra o público atendido e as pesagens.
- Administrador: mantém os cadastros-base e gerencia os acessos.

🎓 Informações Acadêmicas

- Instituição: UNIRUY Wyden
- Polo: Paralela
- Curso: Ciência da Computação
- Projeto: NutriWaste
- Autora: Renata da Conceição Machado
- Ano: 2026

🌱 Considerações Finais

O NutriWaste propõe uma solução para melhorar o controle do desperdício de alimentos em refeitórios corporativos, utilizando modelagem de banco de dados, relacionamentos e indicadores para transformar informações em decisões mais eficientes.

---

NutriWaste – Tecnologia e sustentabilidade no combate ao desperdício de alimentos.
