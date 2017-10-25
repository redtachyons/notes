Arel : 

AST: To store query
Visitor: Produce SQL
Manager: Manipulate AST 

users = Arel::Table.new(:users)
users.project('*').to_sql

 users.project('*').class
 => Arel::SelectManager


users.project('*').ast.class
=> Arel::Nodes::SelectStatement
