## Desafio 12

% Fatos: pai(nome_pai, nome_filho)
pai(joao, maria).
pai(joao, pedro).
pai(pedro, ana).
pai(carlos, joao).

mae(maria, sofia).
mae(ana, lucas).

% Regras derivadas

% X é avô de Z se X é pai de Y e Y é pai ou mãe de Z
avo(X, Z) :- pai(X, Y), (pai(Y, Z); mae(Y, Z)).

% X é irmão de Y se eles têm o mesmo pai e não são a mesma pessoa
irmao(X, Y) :- pai(P, X), pai(P, Y), X \= Y.

% X é descendente de Y se Y é pai ou mãe de X (direto) ou recursivamente
descendente(X, Y) :- pai(Y, X).
descendente(X, Y) :- mae(Y, X).
descendente(X, Y) :- pai(Y, Z), descendente(X, Z).
descendente(X, Y) :- mae(Y, Z), descendente(X, Z).

