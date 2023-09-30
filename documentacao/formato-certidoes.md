# Formato das Certidões em XML

Este documento fornece informações sobre o formato das certidões em XML utilizadas no projeto.

## Estrutura Básica

As certidões em XML seguem uma estrutura básica definida pelos esquemas (XSD) presentes na pasta `esquemas/`. A estrutura geral inclui os seguintes elementos:

- `<certidao>`: Elemento raiz que contém as informações principais da certidão.
- `<registro>`: Elemento que contém os dados do registro objeto da certidão.
- `<registrosAnteriores>`: Elemento para a lista de registros anteriores.
- `<imoveis>`: Elemento que inclui informações sobre os imoveis.
- `<proprietariosOriginais>`: Elemento que inclui informações sobre os proprietários originais do imóvel.
- `<atos>`: Elemento que inclui informações sobre os atos praticados.


## Exemplo de Certidão em XML

Aqui está um exemplo simplificado de uma certidão em XML:

```xml
<certidao>
  <numeroPedido>1</numeroPedido>
  <dataEmissao>2023-09-29</dataEmissao>
  <registro>
    <numero>10</numero>
    <livro>2</livro>
    <cnm/>
    <dataAbertura>2022-04-20</dataAbertura>
  </registro>
  <registrosAnteriores>
    <registroAnterior>
      <numero>6</numero>
      <livro>2</livro>
      <cnm/>
      <dataAbertura>2022-04-19</dataAbertura>
    </registroAnterior>
    <registroAnterior>
      <numero>10</numero>
      <livro>3</livro>
      <cnm/>
      <dataAbertura>2023-04-19</dataAbertura>
    </registroAnterior>
  </registrosAnteriores>
  <imoveis>
    <imovel>
      <urbano>
        <lote>2</lote>
        <quadra>5</quadra>
        <iptu/>
        <im/>
        <area_privativa_principal/>
        <area_privativa_acessoria/>
        <area_privativa_total/>
        <area_uso_comum/>
        <area_total/>
        <area_uso_comum_terreno/>
        <area_uso_exclusivo_terreno/>
        <area_total_terreno/>
        <fracao_ideal/>
        <area_imovel>50.0</area_imovel>
      </urbano>
      <rural>
        <denominacao></denominacao>
        <area></area>
        <cir></cir>
        <ccir></ccir>
        <nirf></nirf>
        <car></car>
      </rural>
    </imovel>
  </imoveis>
  <atos>
    <ato>
      <numero_ato>1</numero_ato>
      <data_ato>2023-06-01</data_ato>
      <denominacao>averbacao</denominacao>
      <partes/>
    </ato>
    <ato>
      <numero_ato>2</numero_ato>
      <data_ato>2023-07-01</data_ato>
      <denominacao>compra e venda</denominacao>
      <partes>
        <parte>
          <qualificacao>transmitente</qualificacao>
          <percentual>100.0</percentual>
          <pessoa_fisica>
            <nome>nome pessoa</nome>
            <cpf>00000000000</cpf>
          </pessoa_fisica>
          <pessoa_juridica/>
        </parte>
        <parte>
          <qualificacao>adquirente</qualificacao>
          <percentual>100.0</percentual>
          <pessoa_fisica>
            <nome>nome pessoa</nome>
            <cpf>00000000000</cpf>
          </pessoa_fisica>
          <pessoa_juridica/>
        </parte>
      </partes>
    </ato>  
  </atos>
</certidao>