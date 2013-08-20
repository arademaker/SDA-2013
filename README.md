
# Article SDA 2013 (conference version)

## geral

+ enfase na geração dos RDFs e transformações
- enfase no git
+ o que foi feito 
- promessa e ideia de que nada ainda foi feito

## TODO: 

1. Jekyll e porque yaml+markdown
2. melhor descrever mapeamento REL->Triples
3. melhor descrever uso de vocabs e ontologias
4. melhorar bibliografias

## D2R casos:

- CPDOC como está? Inside DB to Outside? Outside to what will chance? 

- mapeamento N:M funcionou para alguns casos como:
  ENTREVISTA_ENTREVISTADO, ENTREVISTA_ENTREVISTADOR

- várias tabelas auxiliares com tipos, códigos etc. Ex:
  TIPO_ARQUIVO. Alguns códigos podem estar nas aplicações também? Vide
  próximo item.

- Em DH_CIDADE o que é CD_RBR?

- Nomes de tabelas, se simplificados (remoção de prefixos) irão
  colapsar. Que tabelas são essas? Lixo?

                 orig             new
21     AC_INSTITUICAO     INSTITUICAO
62        INSTITUICAO     INSTITUICAO
36    AC_TIPO_ARQUIVO    TIPO_ARQUIVO
86       TIPO_ARQUIVO    TIPO_ARQUIVO
46    CONDICAO_ACESSO CONDICAO_ACESSO
12 AC_CONDICAO_ACESSO CONDICAO_ACESSO
56             DOADOR          DOADOR
17          AC_DOADOR          DOADOR
23      AC_LOCALIDADE      LOCALIDADE
63         LOCALIDADE      LOCALIDADE

- modularidade dos arquivos RDF gerados. Como podem ser feitos? Por
  sistema? Dentro dos sistemas por entidades etc.

- propriedades compartilhadas e PROV (http://www.w3.org/TR/2013/NOTE-prov-primer-20130430/)

 - dbo_AC_INSTITUICAO_CD_LOGIN_USUSIS (deveria ser FK com dbo.USUARIO?)
 - dbo_AC_INSTITUICAO_DT_ATU_INS

 Usage:

  select distinct ?pred {
    ?x ?pred ?y .
    filter( regex(str(?pred),"LOGIN","i") )
  } 

## Problemas 

http://logics.emap.fgv.br:10035/repositories/cpdoc#node/%3Chttp://cpdoc.fgv.br/sys/dbo/AC_DESCRITOR_ELEITO/6764%3E
http://logics.emap.fgv.br:10035/repositories/cpdoc#node/%3Chttp://cpdoc.fgv.br/sys/dbo/TEMA_ENTREVISTA/1977/1026%3E

Em TEMA_ENTREVISTA => AC_DESCRITOR_ELEITO

