# Sistema de Gestão de Vendas - Documentação e Diagramas

## 1. Diagrama de Casos de Uso

```plantuml
@startuml
left to right direction
skinparam packageStyle rectangle

actor "Administrador" as admin
actor "Usuário" as user
actor "Funcionário" as func
actor "Sistema\n<<Automático>>" as sys

func -up-|> user

rectangle "Sistema de Gestão de Vendas" {
  usecase "UC03: Cadastrar usuário" as uc03
  usecase "UC04: Editar usuário" as uc04
  usecase "UC05: Excluir usuário" as uc05
  usecase "UC06: Consultar usuário" as uc06
  usecase "UC07: Cadastrar produto" as uc07
  usecase "UC08: Editar produto" as uc08
  usecase "UC09: Excluir produto" as uc09
  usecase "UC12: Cancelar venda" as uc12
  usecase "UC13: Gerar relatório" as uc13
  usecase "UC19: Cadastrar categoria" as uc19
  usecase "UC20: Gerenciar estoque" as uc20

  usecase "UC14: Atualizar perfil" as uc14
  usecase "UC15: Recuperar senha" as uc15
  usecase "UC18: Visualizar histórico" as uc18
  usecase "UC01: Fazer login" as uc01
  usecase "UC02: Fazer logout" as uc02
  usecase "UC10: Consultar produto" as uc10

  usecase "UC11: Registrar venda" as uc11
  usecase "UC16: Registrar pagamento" as uc16

  usecase "UC17: Emitir nota fiscal" as uc17
}

admin --> uc03
admin --> uc04
admin --> uc05
admin --> uc06
admin --> uc07
admin --> uc08
admin --> uc09
admin --> uc12
admin --> uc13
admin --> uc19
admin --> uc20

user --> uc14
user --> uc15
user --> uc18
user --> uc01
user --> uc02
user --> uc10

func --> uc11
func --> uc16

uc17 <-- sys
@enduml
