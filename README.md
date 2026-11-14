
# API REST — Armazém do Seu João

Projeto:
https://github.com/felipez3r0/exemplo-api-2ads.git

Etapas 1-10 (14/11/2026)


## Adendos

#### .nvmrc

Força a rodar o node 24 para evitar problemas de versão com o node 26

#### [Phone nullable](https://github.com/Gustavera5/Api-Ads/commit/054e8c83a576bf7352d7d569bce6f9be3ad75880)

Corrige problema no customer.controler.ts:



```
npx tsc --noEmit
src/controllers/customer.controller.ts:21:57 - error TS2345: Argument of type '{ name: string; email: string; phone?: string | undefined; }' is not assignable to parameter of type 'CreateCustomerInput'.
  Types of property 'phone' are incompatible.
    Type 'string | undefined' is not assignable to type 'string | null'.
      Type 'undefined' is not assignable to type 'string | null'.

21       res.status(201).json(await customerService.create(data));
                                                           ~~~~


Found 1 error in src/controllers/customer.controller.ts:21

```

